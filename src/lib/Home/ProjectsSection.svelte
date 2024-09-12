<script lang="ts">
    import Business1 from "$lib/assets/img/Business1.png"
</script>

<section id="projects" class="py-32 bg-neutral-50 text-neutral-950 w-full relative">
    <div class="lg:w-[1200px] max-w-[1200px] flex flex-col justify-center m-auto p-4">
        <h4 class="text-4xl font-bold mb-6">Projects</h4>
        <h2 class="text-2xl mb-2">Businesses I've worked with:</h2>
            <div class="space-y-8">
                <div class="grid grid-cols-1 md:grid-cols-2 bg-neutral-100 p-4 rounded-xl gap-x-0 md:gap-x-4 gap-y-4 md:gap-y-0 border border-neutral-200/70">
                    <div>
                        <h1 class="text-xl font-bold mb-2">Website for a Horse Riding Services Company</h1>
                        <h1 class="text-lg font-bold mb-1">Description:</h1>
                        <p>
                            This project was completed for a German company specializing in leisure services,
                            including horse riding experiences, hosting children's birthday parties, and offering training programs in horse care, riding techniques, and safety.
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
                    <img src={Business1} class="rounded-xl object-cover drop-shadow-xl" alt="business1"/>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 bg-neutral-100 p-4 rounded-xl gap-x-0 md:gap-x-4 gap-y-4 md:gap-y-0 border border-neutral-200/70">
                    <div>
                        <h1 class="text-xl font-bold mb-2">Website for a Company selling Martial Arts Courses (WIP)</h1>
                        <h1 class="text-lg font-bold mb-1">Description:</h1>
                        <p>
                            This website was completed for a martial arts school, which teaches and trains people to become martial arts trainers themselves.
                        </p>
                        <h1 class="text-lg font-bold mb-1 mt-4">Project Goals:</h1>
                        <p>
                            Since this is a pretty huge website, development wise, it is quite a challenge for me to get everything right. From design / frontend to
                            creating a safe backend. Another goal is to make it easy for the user to navigate through the website. For the admins of the website,
                            I also made sure to build an easy to use dashboard, to manage their videos, member access and much more.
                        </p>
                        <h1 class="text-lg font-bold mb-1 mt-4">Technologies Used:</h1>
                        <ul class="list-disc list-inside">
                            <li>Frontend: SvelteKit, TypeScript, TailwindCSS</li>
                            <li>Backend: MySQL, Prism, Lucia Auth</li>
                            <li>Hosting: Ubuntu Server, NGINX</li>
                        </ul>
                    </div>
                    <img src="https://fakeimg.pl/1920x1080" class="rounded-xl object-cover drop-shadow-xl" alt="business1"/>
                </div>
            </div>

        <h2 class="text-2xl mb-2 mt-8">Other projects:</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 rounded-xl gap-x-0 gap-y-4 md:gap-x-4">
            <div class="bg-neutral-100 p-2 border border-neutral-200/70 rounded-xl">
                <h1 class="text-xl font-bold">WIP</h1>
            </div>
            <div class="bg-neutral-100 p-2 border border-neutral-200/70 rounded-xl">
                <h1 class="text-xl font-bold">WIP</h1>
            </div>
            <div class="bg-neutral-100 p-2 border border-neutral-200/70 rounded-xl">
                <h1 class="text-xl font-bold">WIP</h1>
            </div>
        </div>
    </div>
</section>