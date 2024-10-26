<script>
    import { openModal } from "../store";
</script>

<header class="flex flex-col relative z-20 mb-12">
	<div class="max-w-[1400px] mx-auto w-full flex items-center justify-between p-4 py-8">
		<a href="/">
			<h1 class="font-semibold text-xl">
				touris<span class="text-yellow-300">mous</span>
			</h1>
		</a>
        <!---->
		<button  on:click={() => ($openModal = true)} class="md:hidden grid place-items-center">
			<i class="fa-solid fa-bars"></i>
		</button>

		<nav class="hidden md:flex items-center gap-4 lg:gap-6">
			<a href="https://github.com/Tourismous" target="_blank" class="duration-200 hover:text-yellow-300 cursor-pointer">Github</a>
			<a href="#about" class="duration-200 hover:text-yellow-300 cursor-pointer">About</a>
			<a href="#faqs" class="duration-200 hover:text-yellow-300 cursor-pointer">FAQs</a>
			<a href="https://ko-fi.com/tourismousteam" target="_blank" class="duration-200 hover:text-yellow-300 cursor-pointer">Donations</a>
		</nav>
	</div>
</header>
