<script setup lang="ts">
import HeroVectorBottom from "@/assets/images/hero-vector-bottom.svg";
import HeroVectorRight from "@/assets/images/hero-vector-right.svg";
import ArrowTopRight from "@/assets/images/arrow-top-right.svg";
import HeroVectorCenter from "@/assets/images/hero-vector.svg";
import HeroSectionMobile from "./HeroSectionMobile.vue";
</script>

<template>
    <HeroSectionMobile />
    
    <!-- desktop -->
    <section class="relative app-container hidden lg:block">
        <img
        :src="HeroVectorBottom"
        alt="vector image"
        class="absolute left-1/2 top-[-2.5rem] -z-10 h-auto w-[calc(100%-4rem)] -translate-x-1/2 object-contain"
        />    

        <!-- Group the two images together -->
        <div class="absolute w-210 left-[65%] -z-11 top-5 -translate-x-1/2">
            <img
                :src="HeroVectorRight"
                alt=""
                class="h-auto w-auto object-cover"
            />

            <img
                :src="ArrowTopRight"
                alt=""
                class="absolute -right-10 -bottom-10 h-40 w-40 object-cover"
            />

        </div>

        <!-- vector at center -->

        <img
            :src="HeroVectorCenter"
            alt=""
            class="absolute left-1/2 top-[55%] w-auto skew-y-1 -translate-x-1/2 -translate-y-1/2 object-contain"
        />

        <div class="relative h-[85vh] min-h-162 max-h-180">
            <div
                class="absolute inset-x-0 bottom-0 mx-auto flex w-full max-w-360  justify-evenly "
            >
                <h2 class="text-7xl font-extrabold text-secondary">
                Your way to
                </h2>

                <div class="text-brand">
                    <h2 class="text-7xl font-extrabold">better payments</h2>

                    <p class="mt-4 text-3xl">
                        Accept, send, and reconcile <br />
                        payments in one place.
                    </p>
                </div>
            </div>
        </div>

    </section>
</template>