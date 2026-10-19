<script setup lang="ts">
import HeroVectorBottom from "@/assets/images/hero-vector-bottom.svg";
import HeroVectorRight from "@/assets/images/hero-vector-right.svg";
import ArrowTopRight from "@/assets/images/arrow-top-right.svg";
</script>

<template>
  <section class="relative app-container">
    <img
      :src="HeroVectorBottom"
      alt="vector image"
      class="absolute inset-0 -z-10 h-auto w-full object-cover"
    />

    <!-- Group the two images together -->
    <div class="absolute w-220 left-[65%] -z-11 top-5 -translate-x-1/2">
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

    <div class="app-container relative ">
      <!-- <h1>Hero section</h1> -->
    </div>
  </section>
</template>