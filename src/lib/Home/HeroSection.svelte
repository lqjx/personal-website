<script lang="ts">
    import Particles, { particlesInit } from '@tsparticles/svelte';
    import { loadFull } from "tsparticles";

    import {fade, fly} from "svelte/transition";
    import Kawai from "$lib/assets/img/Kawaii2.jpg"

    //let particlesUrl = 'http://foo.bar/particles.json'; // placeholder, replace it with a real url

    let particlesConfig = {
        particles: {
            shape: {
                type: "circle",
            },
            color: {
                value: '#d4d4d4'
            },
            move: {
                enable: true,
                speed: 0.1,
            },
            number: {
                value: 350
            },
            opacity: {
                animation: {
                    enable: true,
                    speed: 1,
                    sync: false,
                },
                value: { min: 0, max: 1 },
            },
            size: {
                value: { max: 2.5, min: 1 },
            },
        },
        preset: "stars",
    };

    let onParticlesLoaded = (event) => {
        const particlesContainer = event.detail.particles;
    };

    void particlesInit(async (engine) => {
        await loadFull(engine);
    });

    function fadeFly(node, { delay = 0, duration = 400, y = -20 } = {}) {
        return {
            delay,
            duration,
            css: t => `
                transform: translateY(${(1 - t) * y}px);
                opacity: ${t};
            `
        };
    }
</script>

<section class="bg-gradient-to-bl from-violet-500 via-violet-400 to-violet-300 flex justify-center h-screen items-center">
    <div class="">
        <Particles
                id="tsparticles"
                class="bg-fixed"
                options="{particlesConfig}"
                on:particlesLoaded="{onParticlesLoaded}"
        />
        <div class="lg:w-[1200px] max-w-[1200px] p-4">
            <div class="flex items-center grid grid-cols-1 md:grid-cols-2 gap-12">
                <div>
                    <h1 transition:fly={{ duration: 1000, y: -20 }} class="text-7xl drop-shadow-md">Hi!<br>
                        I'm daydream
                    </h1>
                    <p transition:fade={{ duration: 1000, delay: 500 }} class="mb-8 mt-4 text-lg">
                        Web Developer, C++ and Reverse Engineering enthusiast
                    </p>
                    <a href="#">
                        <button transition:fade={{ duration: 1000, delay: 1000 }} class="transition flex m-auto text-center
                         bg-gradient-to-tl from-violet-500 via-violet-400 to-violet-300
                         border border-violet-300 border-l-violet-200 border-t-violet-200 border-b-violet-300
                          px-4 py-2.5 rounded-3xl drop-shadow-xl active:scale-95 active:brightness-95

                         hover:bg-gradient-to-tl hover:from-violet-600 hover:via-violet-500 hover:to-violet-400 hover:text-neutral-200
                         hover:border-violet-400 hover:border-l-violet-300 hover:border-t-violet-300 hover:border-b-violet-400
                        ">
                            Visit Blog
                        </button>
                    </a>
                </div>
                <img transition:fadeFly={{ y: -20, duration: 1000 }} src={Kawai} class="flex m-auto w-96 border-2 border-neutral-100 rounded-3xl drop-shadow-xl"  alt="profile-pic"/>
            </div>
            <div class="custom-shape-divider-bottom-1725985162">
                <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none" class="relative bottom-0">
                    <path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" class="shape-fill"></path>
                    <path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" class="shape-fill"></path>
                    <path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" class="shape-fill"></path>
                </svg>
            </div>
        </div>
    </div>
</section>

<style>
    .custom-shape-divider-bottom-1725985162 {
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        overflow: hidden;
        line-height: 0;
        transform: rotate(180deg);
    }

    .custom-shape-divider-bottom-1725985162 svg {
        position: relative;
        display: block;
        width: calc(100% + 1.3px);
        height: 150px;
    }

    .custom-shape-divider-bottom-1725985162 .shape-fill {
        fill: #FAFAFA;
    }
</style>