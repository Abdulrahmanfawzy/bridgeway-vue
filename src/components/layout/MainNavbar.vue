<script setup lang="ts">
import Logo from "../../assets/images/logo.svg";
import ArrowIcon from "../../assets/images/arrow.svg";
import BaseButton from "../ui/BaseButton.vue";

const links = [
  { label: "Benefits", href: "#benefits" },
  { label: "Contact Us", href: "#contactUs" },
];
</script>

<template>
  
<nav class="absolute inset-x-0 top-0 z-50">
  <div
    class="app-container flex h-32 items-center justify-between lg:h-28"
  >
    <div class="lg:flex items-center gap-6 lg:gap-20">
      <img
        :src="Logo"
        alt="Bridgeway Logo"
        class="w-40 shrink-0 my-3 -mt-1 lg:mt-0 lg:my-0 lg:w-auto"
      />

      <ul class="flex items-center -mb-10 lg:mb-0 gap-6 lg:gap-20">
        <li v-for="link in links" :key="link.href">
          <a
            :href="link.href"
            class="text-white transition-colors hover:text-secondary"
          >
            {{ link.label }}
          </a>
        </li>
      </ul>
    </div>

    <BaseButton
      class="shrink-0 px-7 font-bold"
      label="Get Started"
      variant="primary"
    >
      <template #icon>
        <img :src="ArrowIcon" alt="" class="h-3 w-3" />
      </template>
    </BaseButton>
  </div>
</nav>

</template>