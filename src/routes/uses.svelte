<script>
	import Container from '../components/UI/Container.svelte'
	import PageHeading from '../components/UI/PageHeading.svelte'
	import PageFooter from '../components/UI/PageFooter.svelte'
	import PageContent from '../components/UI/PageContent.svelte'

	const content = {
		heading: 'Gear/Apps I like to use',
	}

</script>

<svelte:head>
	<title>Brian Casey | Web Developer | Uses</title>
</svelte:head>

<Container>
	<PageHeading heading={'Uses'} />

	<PageContent {content} >
		<ul>
			<li>Work Computer: HP Elitebook G6</li>
			<li>Home Computer: 2015 13" MacBook Pro</li>
			<li>Phone: Apple iPhone XS</li>
			<li>Headphones: Apple Airpods</li>
			<li>Notes App: Notion</li>
			<li>Keyboard: Keychron K1</li>
			<li>Laptop Stand: Roost 2.0</li>
			<li>Microphone: Audiotechnica ATR2100</li>
		</ul>
	</PageContent>

	<PageFooter />
</Container>


