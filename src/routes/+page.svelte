<script lang="ts">
    import {fade} from "svelte/transition";
    import HeroSection from "$lib/Home/HeroSection.svelte";
    import AboutSection from "$lib/Home/AboutSection.svelte";
</script>

<div transition:fade>
    <HeroSection/>
    <AboutSection/>
</div>