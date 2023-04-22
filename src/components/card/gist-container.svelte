<script lang="ts">
	import Icon from '@iconify/svelte';
	import { Profile4, Profile5 } from '../../assets/images';
	import type { IGistChat } from '../types';
	import GistChat from './atoms/gist-chat.svelte';

	let gistChat: IGistChat[] = [
		{
			image: Profile5,
			message: "can't wait the timeline deisign"
		},
		{
			image: Profile4,
			message: 'can I get a link?'
		}
	];
</script>

<div class="px-6">
	<div class="flex gap-1 mt-5 ml-3">
		<p>Wojciech Zielisnki</p>
		<p class="text-zinc-400">updated T-29 status to</p>
		<p class="text-blue-300">In Progress</p>
	</div>

	<div class="flex items-center gap-4 px-8 py-4">
		<div
			class="bg-zinc-800 rounded-xl py-4 px-6 flex flex-col gap-3 border-t border-zinc-700 shadow-sm shadow-black"
		>
			<div class="flex gap-2 text-zinc-300 items-center">
				<Icon icon="pajamas:branch" class="text-xl rotate-180" />
				<h2 class="text-xl">T-29</h2>
			</div>
			<div class="flex gap-3 items-center">
				<div class="outline-blue-400 outline w-4 h-4 rounded-full self-start mt-2" />
				<div class="flex flex-col gap-1">
					<h2 class="text-xl">Timeline View</h2>
					<p class="text-sm text-zinc-400">Spot timing conflicts and plan deadlines</p>
				</div>
			</div>
		</div>

		<div class="flex gap-2">
			<div class="flex gap-1">
				<div class="rounded-full bg-zinc-800 w-7 h-7 flex justify-center items-center">
					<Icon icon="twemoji:bear" />
				</div>
				<p class="text-zinc-400">2</p>
			</div>

			<div class="flex gap-1">
				<div class="rounded-full bg-zinc-800 w-7 h-7 flex justify-center items-center">
					<Icon icon="twemoji:coin" />
				</div>
				<p class="text-zinc-400">5</p>
			</div>
		</div>
	</div>
	<div class="relative px-14 mt-1">
		<div class="h-1 bg-zinc-700 w-32 z-10 rotate-90 top-12 left-1.5 rounded-full absolute" />
		<div class="flex flex-col gap-4">
			<div class="flex flex-col gap-5 z-20">
				{#each gistChat as chat}
					<GistChat src={chat.image} message={chat.message} />
				{/each}
			</div>
			<h2
				class="px-10 text-blue-400 text-lg font-medium hover:text-blue-300 duration-150 transition-all"
			>
				2 more replies
			</h2>
		</div>
	</div>
</div>
