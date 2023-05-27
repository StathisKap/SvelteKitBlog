<script>
	import '../app.postcss';
	import 'open-props/style';
	import 'open-props/normalize';
	import 'open-props/buttons';
	import '../app.css';
	import Footer from '$lib/components/Footer.svelte';
	import Header from '$lib/components/Header.svelte';
	import Transitions from '$lib/components/Transitions.svelte';

	export let data;
</script>

<div class="h-screen grid grid-rows-[auto,1fr,auto] mx-auto px-8">
	<Header />
	<main class="my-8">
		<Transitions url={data.url}>
			<slot />
		</Transitions>
	</main>
	<Footer />
</div>
