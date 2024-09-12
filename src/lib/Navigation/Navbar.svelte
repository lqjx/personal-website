<script lang="ts">
    import {onMount} from "svelte";
    import HeroSection from "$lib/Home/HeroSection.svelte";
    import AboutSection from "$lib/Home/AboutSection.svelte";
    import ProjectsSection from "$lib/Home/ProjectsSection.svelte";

    let scrolled: boolean = false;

    const handleScroll = () => {
        scrolled = window.scrollY > 0;
    };

    onMount(() => {
        window.addEventListener("scroll", handleScroll);

        return () => {
            window.removeEventListener("scroll", handleScroll);
        }
    });
</script>

<nav class="fixed flex justify-between items-center px-12 w-full transition-all duration-300 ease-in-out z-50 border-transparent
    {scrolled ? 'backdrop-blur-lg h-16 bg-neutral-50/20 text-neutral-950' : 'bg-transparent h-24'}">
    <div class="flex items-center justify-between space-x-2">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 15a4.5 4.5 0 0 0 4.5 4.5H18a3.75 3.75 0 0 0 1.332-7.257 3 3 0 0 0-3.758-3.848 5.25 5.25 0 0 0-10.233 2.33A4.502 4.502 0 0 0 2.25 15Z" />
        </svg>
        <a href="./" class="font-bold text-xl">DAYDREAM.DEV</a>
    </div>
    <div class="space-x-4">
        <a href="#hero" class="text-lg hover:box-shadow-md hover:underline hover:underline-offset-8 hover:decoration-2
        {scrolled ? 'decoration-neutral-950' : 'decoration-neutral-50'}">Home
        </a>
        <a href="#about" class="text-lg hover:box-shadow-md hover:underline hover:underline-offset-8 hover:decoration-2
        {scrolled ? 'decoration-neutral-950' : 'decoration-neutral-50'}">About
        </a>
        <a href="#projects" class="text-lg hover:box-shadow-md hover:underline hover:underline-offset-8 hover:decoration-2
        {scrolled ? 'decoration-neutral-950' : 'decoration-neutral-50'}">Projects
        </a>
        <a href="#contact" class="text-lg hover:box-shadow-md hover:underline hover:underline-offset-8 hover:decoration-2
        {scrolled ? 'decoration-neutral-950' : 'decoration-neutral-50'}">Contact
        </a>
    </div>
</nav>