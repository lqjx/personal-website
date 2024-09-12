<script lang="ts">
    import {fade} from "svelte/transition";
    import HeroSection from "$lib/Home/HeroSection.svelte";
    import AboutSection from "$lib/Home/AboutSection.svelte";
    import ProjectsSection from "$lib/Home/ProjectsSection.svelte";
    import Navbar from "$lib/Navigation/Navbar.svelte";
    import Footer from "$lib/Footer.svelte";
</script>

<div transition:fade class="">
    <Navbar/>
    <HeroSection/>
    <AboutSection/>
    <ProjectsSection/>
    <Footer/>
</div>