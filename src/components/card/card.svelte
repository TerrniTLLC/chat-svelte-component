<script lang="ts">
	import CardContainer from './card-container.svelte';
	import CardFooter from './card-footer.svelte';
	import CardTilebar from './card-tilebar.svelte';
	import ChatContainer from './chat-container.svelte';
	import GistContainer from './gist-container.svelte';
	import type { IChat } from '../types';
	import { Profile1, Profile2, Profile3, Profile4 } from '../../assets/images';

	let chatData1: IChat[] = [
		{
			name: 'Terrnit',
			date: 'Oct 22 8:45 AM',
			image: Profile1,
			message: 'wow pretty good despite the lack of direction',
			tag: '@Ronn'
		},
		{
			name: '@Jarvis',
			date: 'Oct 22 8:45 AM',
			image: Profile2,
			message:
				'Next 2 cycles by squad. Best place to see what each squad is working on right now and what`s on desk for next cycle '
		}
	];

	let chatData2: IChat[] = [
		{
			name: 'seocat',
			date: 'Oct 23 5:45 AM',
			image: Profile3,
			message: "oh man I can't wait for timeline design "
		},
		{
			name: '@Jarvis',
			date: 'Oct 22 8:45 AM',
			image: Profile4,
			message: 'Lmao'
		}
	];
</script>

<CardContainer>
	<CardTilebar />
	<ChatContainer chatData={chatData1} />
	<GistContainer />
	<ChatContainer chatData={chatData2} />
	<CardFooter />
</CardContainer>
