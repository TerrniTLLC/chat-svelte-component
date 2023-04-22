<script lang="ts">
	import ProfilePreview from './profile-preview.svelte';
	import type { IChat } from '../../types';

	export let chatData: IChat[];
</script>

{#each chatData as chat}
	<div class="bg-secondary w-full rounded-2xl gap-4 py-4 px-3 flex">
		<ProfilePreview size="normal" src={chat.image} />
		<div class="text-left flex flex-col items-start">
			<div class="flex gap-2 justify-center">
				<h3 class="text-sm font-bold">{chat.name}</h3>
				<p class="text-sm text-zinc-400 font-medium">Oct 22 8:45 AM</p>
			</div>
			<div class="flex gap-1">
				<p class="text-zinc-300 break-all">{chat.message}</p>
				{#if chat.tag}
					<p class="text-yellow-400 bg-yellow-300/20 rounded-md px-1 font-medium break-all">
						{chat.tag}
					</p>
				{/if}
			</div>
		</div>
	</div>
{/each}
