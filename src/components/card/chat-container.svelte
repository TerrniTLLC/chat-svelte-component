<script lang="ts">
	import ChatBubble from './atoms/chat-bubble.svelte';
	import type { IChat } from '../types';

	export let chatData: IChat[];
</script>

<div class="px-6 mt-4 gap-3 flex flex-col">
	<ChatBubble {chatData} />
</div>
