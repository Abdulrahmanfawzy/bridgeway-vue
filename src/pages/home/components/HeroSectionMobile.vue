<script setup lang="ts">
import HeroVectorMobile from "@/assets/images/hero-vector-mobile.svg";
import ArrowTopRight from "@/assets/images/arrow-top-right.svg";
</script>

<template>
    <!-- shape brand color in mobile -->
    <div class="app-container absloute left-0 top-0 block lg:hidden inset-0 w-full rounded-b-[60px] bg-brand pb-20">

        <div class="pt-40 mb-10 text-secondary">
            <h2 class="text-4xl font-extrabold ">
                Your way to <br>
                better payments
            </h2>

            <p class="mt-4 text-lg text-white">
                Accept, send, and reconcile
                payments in one place.
            </p>
        </div>

        <div class="grid grid-cols-3 items-end">

            <img
                :src="HeroVectorMobile"
                alt="vector image mobile"
                class="h-55 w-full col-span-2 object-cover rounded-4xl"
            />   
            <img
                :src="ArrowTopRight"
                alt="vector image mobile"
                class="col-span-1 rounded-4xl"
            />   
        </div> 

    </div>
</template>