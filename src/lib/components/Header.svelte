<script lang="ts">
	import * as config from '$lib/config';
	import Toggle from './Toggle.svelte';
</script>

<nav class="px-8 sm:flex sm:justify-between py-2">
	<a href="/">
		<b>{config.title}</b>
	</a>
	<ul class="mx-8 sm:flex sm:gap-8 sm:mx-0 list-disc">
		<li>
			<a href="/about">About</a>
		</li>
		<li>
			<a href="/contact">Contact</a>
		</li>
		<li>
			<a href="/rss.xml" target="_blank">RSS</a>
		</li>
	</ul>
	<Toggle />
</nav>

<style>
	nav > ul > li > a {
		color: var(--text-2);
	}
</style>
