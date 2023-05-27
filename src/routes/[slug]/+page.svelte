<script lang="ts">
	import { formatDate } from '$lib/utlis';

	export let data;
</script>

<svelte:head>
	<title>{data.meta.title}</title>
	<meta property="og:type" content="article" />
	<meta property="og:title" content={data.meta.title} />
</svelte:head>

<article class="max-w-prose mx-auto">
	<hgroup>
		<h1 class="text-5xl mb-4 capitalize">{data.meta.title}</h1>
		<p class="text-gray-400">Published at {formatDate(data.meta.date)}</p>
	</hgroup>

	<div class="flex gap-3 mt-8">
		{#each data.meta.categories as category}
			<span class="surface-4 py-2 px-3 rounded-2xl">&num;{category}</span>
		{/each}
	</div>

	<div class="prose">
		<svelte:component this={data.content} />
	</div>
</article>
