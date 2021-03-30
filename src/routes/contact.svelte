<script>
	import Container from '../components/UI/Container.svelte'
	import PageHeading from '../components/UI/PageHeading.svelte'
	import PageFooter from '../components/UI/PageFooter.svelte'
	import PageContent from '../components/UI/PageContent.svelte'

	const content = {
		heading: 'Get in touch',
	}


</script>

<style>
	p {
		font-size: 1.2rem;
	}
</style>

<svelte:head>
	<title>Brian Casey | Web Developer | Contact</title>
</svelte:head>

<Container>
	<PageHeading heading={'Contact'} />

	<PageContent {content} >
		<p>Do you have a project you want me to work on? Want do hire me?</p>
		<p>Send me an email at briancasey@outlook.com with the details.</p> 
	</PageContent>

	<PageFooter />
</Container>

