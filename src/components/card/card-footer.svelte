<script lang="ts">
	import Icon from '@iconify/svelte';
	import { Profile5 } from '../../assets/images';
	import ProfilePreview from './atoms/profile-preview.svelte';
</script>

<div class="flex px-6 my-8 gap-3">
	<ProfilePreview size="normal" src={Profile5} />
	<div class="border border-zinc-800 w-full rounded-lg items-center flex pl-3 pr-2">
		<input
			type="text"
			placeholder="Write a comment"
			class="bg-transparent outline-none text-zinc-300 placeholder:text-zinc-800 w-full"
		/>
		<div class="flex gap-4 items-center text-zinc-500">
			<div class="flex text-2xl gap-3">
				<Icon
					icon="ph:text-a-underline-bold"
					class="hover:text-zinc-300 duration-150 transition-all"
				/>
				<Icon
					icon="ri:emoji-sticker-fill"
					class="hover:text-zinc-300 duration-150 transition-all"
				/>
				<Icon
					icon="heroicons-outline:paper-clip"
					class="hover:text-zinc-300 duration-150 transition-all"
				/>
			</div>
			<button
				class="w-9 h-9 rounded-lg bg-zinc-700 flex justify-center items-center hover:text-zinc-300 duration-150 transition-all hover:bg-zinc-800/70 text-zinc-500"
			>
				<Icon icon="bxl:telegram" class=" text-2xl rotate-[10deg]" />
			</button>
		</div>
	</div>
</div>
