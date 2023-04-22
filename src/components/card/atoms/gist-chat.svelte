<script lang="ts">
	import ProfilePreview from './profile-preview.svelte';

	export let src: string;
	export let message: string;
</script>

<div class="flex gap-3 items-center">
	<ProfilePreview {src} size="small" />
	<p class="text-zinc-300 text-lg">{message}</p>
</div>
