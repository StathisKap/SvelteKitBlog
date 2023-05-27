<script lang="ts">
	import { fly } from 'svelte/transition';
	import { Moon, Sun } from 'lucide-svelte';
	import { theme, toggleTheme } from '$lib/theme';
</script>

<button on:click={toggleTheme} aria-label="Toggle Theme" class="border-0 shadow-none">
	{#if $theme === 'dark'}
		<div in:fly={{ y: 10 }} class="flex gap-2">
			<Sun />
			<span>Light</span>
		</div>
	{:else}
		<div in:fly={{ y: -10 }} class="flex gap-2">
			<Moon />
			<span>Dark</span>
		</div>
	{/if}
</button>
