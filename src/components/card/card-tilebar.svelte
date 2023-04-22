<script lang="ts">
	import Icon from '@iconify/svelte';
	import TilebarTag from './atoms/tilebar-tag.svelte';
	import ProfilePreview from './atoms/profile-preview.svelte';

	import { Profile1, Profile2, Profile3, Profile4, Profile5 } from '../../assets/images/index';

	let profileArray: string[] = [Profile1, Profile2, Profile3, Profile4, Profile5];
</script>

<div class="py-9 px-7 rounded-t-xl h-16 border-b border-zinc-900 flex justify-between">
	<div class="flex gap-2 w-full items-center">
		<TilebarTag content="design">
			<Icon icon="material-symbols:grid-3x3" class="rotate-[75deg] text-blue-400 text-lg" />
		</TilebarTag>
		<TilebarTag content="32">
			<Icon icon="material-symbols:man-4-rounded" class="text-zinc-400 text-lg" />
		</TilebarTag>
	</div>
	<div class="flex items-center w-full -space-x-1">
		{#each profileArray as profile}
			<ProfilePreview src={profile} size="small" />
		{/each}
	</div>

	<div class="flex gap-3 items-center w-fit">
		<Icon
			icon="mingcute:search-2-fill"
			class="text-zinc-400 hover:text-zinc-200 duration-150 transition-all text-xl"
		/>
		<Icon
			icon="ph:bookmark-simple-bold"
			class="text-zinc-400 hover:text-zinc-200 duration-150 transition-all text-xl"
		/>
		<Icon
			icon="mdi:dots-horizontal"
			class="text-zinc-400 hover:text-zinc-200 duration-150 transition-all text-xl"
		/>
	</div>
</div>
