<script lang="ts">
	export let content: string | number;
</script>

<div class="flex gap-1 items-center bg-zinc-900 w-fit h-6 px-1 rounded justify-center">
	<slot />
	<p class="text-sm font-medium text-zinc-400">{content}</p>
</div>
