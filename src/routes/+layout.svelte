<script>
	import '../assets/main.css';
	import Footer from '../components/footer.svelte';
	import Head from '../components/head.svelte';
</script>

<Head />
<main class="bg-[#6c7279] h-screen">
	<slot />
	<Footer />
</main>
