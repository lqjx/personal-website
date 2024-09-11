<script lang="ts">
    import Business1 from "$lib/assets/img/Business1.png"

    let isLoggedIn: boolean = false;
</script>

<section class="py-32 bg-neutral-50 text-neutral-950 w-full relative">
    <div class="lg:w-[1200px] max-w-[1200px] flex flex-col justify-center m-auto p-4">
        <h4 class="text-4xl font-bold mb-6">Projects</h4>
        <h2 class="text-2xl mb-2">Businesses I've worked with:</h2>
        {#if isLoggedIn}
            <p>Since I value privacy, please contact me to request access to the projects I have completed for companies.</p>
        {:else}
        <div class="space-y-4">
            <div class="grid grid-cols-1 md:grid-cols-2 bg-neutral-100 p-4 rounded-xl gap-y-4 md:gap-y-0">
                <div>
                    <h1 class="text-xl font-bold mb-2">Website for a Horse Riding Company</h1>
                    <h1 class="text-lg font-bold mb-1">Description:</h1>
                    <p>
                        This project was completed for a German company specializing in leisure services,
                        including horse riding experiences, hosting children's birthday parties, and offering training programs in horse care, riding techniques, and safety
                    </p>
                    <h1 class="text-lg font-bold mb-1 mt-4">Project Goals:</h1>
                    <p>
                        This client needed a simple website, to boost it's online bookings and to showcase their service, aiming on accessibility and ease of use.
                    </p>
                    <h1 class="text-lg font-bold mb-1 mt-4">Technologies Used:</h1>
                    <ul class="list-disc list-inside">
                        <li>Frontend: SvelteKit, TypeScript, TailwindCSS</li>
                        <li>Backend: None</li>
                        <li>Hosting: Ubuntu Server, NGINX</li>
                        <li>Booking Integration: API synced with Google Calendar</li>
                    </ul>
                </div>
                <img src={Business1} class="border-neutral-100 rounded-xl drop-shadow-xl" alt="business1"/>
            </div>
        </div>
        {/if}

        <h2 class="text-2xl mb-2 mt-8">Other projects:</h2>
    </div>
</section>