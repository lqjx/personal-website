<script>
    import {fade} from "svelte/transition";
    import "../app.css";
</script>

<div transition:fade class="bg-black text-neutral-50 font-jetbrains">
    <slot />
</div>