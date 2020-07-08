<script>
import { fly, fade } from 'svelte/transition'
import { firstLoad } from '../store/stores.js'

export let heading

let isFirstLoad
let duration

const unsubcribe = firstLoad.subscribe(value => {
	isFirstLoad = value
})

$: isFirstLoad ? duration = 500 : duration = 0

</script>

<style>	
	.wrapper {
		filter: drop-shadow(0px 3px 5px rgba(0,0,0,0.4));
		width: 100%;
	}

	header {
	/* background-color: #999999; */
	position: relative;
	z-index: 1;
	display: flex;
	flex-direction: column;
	align-items: center;
	background-image: linear-gradient(
		to right bottom,
		rgba(153,153,153, 1),
		rgba(153,153,153, 0.7));
	background-size: cover;
	background-position: top;
	clip-path: polygon(0 0, 100% 0%, 100% 40%, 35% 100%, 0% 55%);
	width: 100%;
	}

	.me {
	font-family: 'Montserrat', sans-serif;
	font-weight: 500;
	font-size: 3rem;
	line-height: 2;
	text-transform: uppercase;
	margin-bottom: 2.5rem;
	/* color: rgba(127,127,190,1); */
	color: white;
	}	

</style>

<span class="wrapper">
	<header in:fade="{{duration: duration}}">
		<div class="me" out:fade="{{duration: 300}}">
			{#each heading as char, i}
				<span
					in:fade="{{delay: 300 + i * 100, duration: 300}}"
				>{char}</span>
			{/each}
		</div>
	</header>
</span>

<!-- out:fly="{{y: -20, duration: 300}}" in:fade="{{duration: 300}}" -->
<!-- out:fly="{{y: -20, duration: 300}}" -->