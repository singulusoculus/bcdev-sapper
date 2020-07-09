<script>
	import { fadeIn, fadeOut } from './pageFade.js'

	let canRender

	setTimeout(() => {
		canRender = true
	}, 300)
</script>

<style>
	.container {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		position: relative;
		/* height: 100vh; */
		min-height: 100vh;
	}
</style>

{#if canRender}
	<div class="container" >
		<slot></slot>
	<!-- in:fadeIn out:fadeOut -->
	</div>
{/if}
