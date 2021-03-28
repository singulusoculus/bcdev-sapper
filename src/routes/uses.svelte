<script>
	import Container from '../components/UI/Container.svelte'
	import PageHeading from '../components/UI/PageHeading.svelte'
	import PageFooter from '../components/UI/PageFooter.svelte'
	import PageContent from '../components/UI/PageContent.svelte'
	import SkillsGrid from '../components/UI/SkillsGrid.svelte'

	const gear = {
		heading: 'Gear/Apps I like to use',
	}

	const skills = {
		heading: 'Technical Skills'
	}

</script>

<style>

</style>

<svelte:head>
	<title>Brian Casey | Web Developer | Uses</title>
</svelte:head>

<Container>
	<PageHeading heading={'Uses'} />

	<PageContent content={gear} >
		<ul>
			<li>Work Computer: HP Elitebook G6</li>
			<li>Home Computer: 2015 13" MacBook Pro</li>
			<li>Phone: Apple iPhone 12</li>
			<li>Headphones: Apple Airpods</li>
			<li>Notes App: Notion</li>
			<li>Keyboard: Keychron K1</li>
			<li>Laptop Stand: Roost 2.0</li>
			<li>Microphone: Audiotechnica ATR2100</li>
		</ul>
	</PageContent>

	<PageContent content={skills}>
		<SkillsGrid />
		<!-- <ul>
			<li>Svelte</li>
			<li>JS</li>
			<li>CSS</li>
			<li>HTML</li>
			<li>PHP</li>
			<li>WordPress</li>
			<li>SASS</li>
			<li>Git</li>
			<li>SQL Server</li>
			<li>mySQL</li>
			<li>Dynamics SL</li>
			<li>SharePoint</li>
			<li>SSRS</li>
			<li>jQuery</li>
			<li>Node.js</li>
			<li>Vue</li>
			<li>React</li>
			<li>SQLite</li>
			<li>IBM Cognos</li>
			<li>Python</li>
		</ul> -->
	</PageContent>

	<PageFooter />
</Container>


