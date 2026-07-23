<script lang="ts">
	import './layout.css';
	import { page } from '$app/state';
	import favicon from '$lib/assets/favicon.svg';
	import Nav from "$lib/components/Nav.svelte"
	import Footer from "$lib/components/Footer.svelte"

	let { children } = $props();

	let atHome = page.route.id === "/";
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
    <title>Azalea Media Server - Free, Open Source Media Server</title>
</svelte:head>

<div class="flex min-h-screen flex-col">
    <header class="flex items-center justify-between w-full">
        <section class="flex items-center text-2xl font-bold w-20" style="font-family: sans;">
            <img src={favicon} class="h-12 p-2" />
            <span>Azalea</span>
        </section>
        <Nav />
        <section class="w-20"></section>
    </header>
    <main class="flex flex-1 flex-col justify-between w-full">
        <section class="flex flex-col items-center w-full flex-1 p-10 gap-15 *:flex *:flex-col *:w-200 *:gap-3">
            {@render children()}
        </section>
        <Footer />
    </main>
</div>
