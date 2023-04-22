<script lang="ts">
	export let size: 'small' | 'normal';
	export let src: string;
</script>

<img
	{src}
	alt={src}
	class={`${size == 'small' ? 'w-7 h-7 ' : 'h-12 w-12'} rounded-full outline outline-main`}
/>
