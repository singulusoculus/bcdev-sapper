<script>
	import { fadeIn, fadeOut } from '../components/UI/pageFade.js'
	import Bookend from '../components/Timeline/Bookend.svelte'
	import JobTitle from '../components/Timeline/JobTitle.svelte'
	import Moment from '../components/Timeline/Moment.svelte'
	import Technology from '../components/Timeline/Technology.svelte'

	const timeline = [
		{
			component: Bookend,
			options: {
				title: 'Into the future'
			}
		},
		{
			component: JobTitle,
			options: {
				title: 'Web Developer',
				desc: 'I like to make websites and web apps.'
			}
		},
		{
			component: Moment,
			options: {
				title: 'Release Top Nine v2.0',
				desc: null,
				date: 2/1/2020,
				link: '/', // eventual link to project page
				image: null 
			}
		},
		{
			component: Technology,
			options: {
				title: 'Svelte',
				desc: null,
				date: 1/15/20,
				link: '/', // link to svelte.dev
				image: '' // link to image
			}
		},
		{
			component: Bookend,
			options: {
				title: 'In my beginning, I was born',
			}
		}
	]
</script>

<style>

</style>

<svelte:head>
	<title>Brian Casey | Web Developer</title>
</svelte:head>

<div in:fadeIn out:fadeOut>
	<h1>HOME</h1>

	{#each timeline as segment}
		<svelte:component this={segment.component} options={segment.options} />
	{/each}
</div>



