<script lang="ts">
	import { page } from '$app/stores';
</script>

<div class="h-full grid place-content-center">
	<h1 class="text-5xl">{$page.status}: {$page.error?.message}</h1>
</div>
