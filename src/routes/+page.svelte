<script lang="ts">
    import {fade} from "svelte/transition";
    import HeroSection from "$lib/Home/HeroSection.svelte";
    import AboutSection from "$lib/Home/AboutSection.svelte";
    import ProjectsSection from "$lib/Home/ProjectsSection.svelte";
</script>

<div transition:fade class="">
    <HeroSection/>
    <AboutSection/>
    <ProjectsSection/>
</div>