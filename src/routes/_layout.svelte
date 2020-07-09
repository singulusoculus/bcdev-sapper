<script>
	import Nav from '../components/UI/Nav.svelte';
	import { firstLoad } from '../components/store/stores.js'

	export let segment;

	setTimeout(() => {
		firstLoad.set(false)
	}, 2000);


</script>

<style>
	.page-wrapper {
		display: flex;
		/* height: 100vh;
		justify-content: space-between; */
	}

	main {
		flex: 1 1 auto;
		position: relative;
		/* overflow: auto; */
		box-sizing: border-box;
		/* flex-grow: 1; */
	}

	@media only screen and (max-width: 960px) {
		.page-wrapper {
			flex-direction: column;
		}
	}
</style>

<div class="page-wrapper">
	<Nav {segment}/>

	<main>
		<slot></slot>
	</main>
</div>
