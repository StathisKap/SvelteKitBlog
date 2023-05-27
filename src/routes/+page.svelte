<script lang="ts">
	import * as config from '$lib/config';
	import { formatDate } from '$lib/utlis';
	export let data;
</script>

<svelte:head>
	<title>{config.title}</title>
</svelte:head>

<section>
	<ul class="grid gap-8">
		{#each data.posts as post}
			<li class="max-w-16 border-b-2 pb-8 last:border-b-0 border-gray-800">
				<a href={post.slug} class="capitalize text-4xl text-purple-400">{post.title}</a>
				<p class="text-gray-400">{formatDate(post.date)}</p>
				<p class="mt-3">{post.description}</p>
			</li>
		{/each}
	</ul>
</section>
