<script>
    import {fade} from "svelte/transition";
    import "../app.css";
    import Navbar from "../lib/Navigation/Navbar.svelte";
</script>

<div transition:fade class="bg-black text-neutral-50 font-jetbrains">
    <Navbar/>
    <slot />
</div>