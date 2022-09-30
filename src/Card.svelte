<svelte:options tag="design-card" />
<script>
	export let title="just a title";
	export let content="just some random text";
	function onClick() {
		this.dispatchEvent(new CustomEvent('card-click',{composed:true}))
	}
</script>

<div class="card" on:click={onClick}>
	<h1>{title}</h1>
	<p>{content}</p>
</div>

<style>
	.card {
		border:solid rgb(75, 113, 209) 5px;
		box-shadow: 1px 1px;
		border-radius: 10px;
		width: 200px;
		padding: 5px;
		text-align: center;
	}
</style>