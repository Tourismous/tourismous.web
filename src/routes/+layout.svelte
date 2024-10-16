<script>
    import '../app.css';
    import Footer from '../components/Footer.svelte';
    import Header from '../components/Header.svelte';
    import { openModal } from "../store";

    let y;
    $: outerHeight = 0;

    function reroute(href) {
        $openModal = false;
        window.location.href = href;
    }

    function openExternalLink(url) {
        window.open(url, '_blank');
        $openModal = false;
    }
</script>

{#if $openModal}
<div class="fixed top-0 left-0 w-screen h-screen border-b bg-white z-50 flex flex-col gap-8 p-5 px-8 md:hidden">
    <div class="flex items-center justify-between gap-4 border-b pb-2">
        <h1 class="font-semibold text-xl">
            touris<span class="text-yellow-300">mous</span>
        </h1>
        <button
            on:click={() => ($openModal = false)}
            class="outline-none border-none"
        >
            <i class="fa-solid fa-xmark text-2xl"></i>
        </button>
    </div>
    <div class="flex flex-col gap-4 flex-1">
    <button
        on:click={() => openExternalLink('https://github.com/Tourismous')}
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
    >
        <p
            class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold"
        >
        Github <i class="fa-solid fa-chevron-right text-xl pl-4" />
        </p>
    </button>
    <button
        on:click={() => reroute("#about")}
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
    >
        <p
            class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold"
        >
        About <i class="fa-solid fa-chevron-right text-xl pl-4" />
        </p>
    </button>
    <button
        on:click={() => reroute("#faqs")}
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
    >
        <p
            class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold"
        >
            FAQs <i class="fa-solid fa-chevron-right text-xl pl-4" />
        </p>
    </button>

    <button
        on:click={() => openExternalLink('https://ko-fi.com/tourismousteam')}
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
    >
        <p
            class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold"
        >
            Donations <i class="fa-solid fa-chevron-right text-xl pl-4" />
        </p>
    </button>
</div>
</div>
{/if}
{#if y > outerHeight}
    <div class="bg-white fixed top-0 left-0 w-full flex flex-col z-20 px-4 fadeIn">
        <Header/>
    </div>
{/if}
<slot />
<Footer />
<svelte:window bind:scrollY={y} bind:outerHeight />