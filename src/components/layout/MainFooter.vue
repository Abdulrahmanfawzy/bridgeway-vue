<script setup lang="ts">
import Linkedin from "@/assets/images/linkedin.svg";
import Facebook from "@/assets/images/facebook.svg";
import Insta from "@/assets/images/insta.svg";
import FooterImage from "@/assets/images/footer.svg";

const socialLinks = [
  { name: "LinkedIn", icon: Linkedin, href: "#" },
  { name: "Facebook", icon: Facebook, href: "#" },
  { name: "Instagram", icon: Insta, href: "#" },
];
</script>

<template>
  <footer class="app-container mt-10 lg:mt-40">
    <div class="flex justify-between flex-col gap-5 lg:gap-0 lg:flex-row mb-30 lg:mb-60">
      <div>
        <h2 class="text-3xl font-bold">Bridgeway</h2>
        <p class="text-gray-600">
          Everything payments, on one bridge
        </p>
      </div>

      <div class="flex items-center gap-4">
        <a
          v-for="social in socialLinks"
          :key="social.name"
          :href="social.href"
          :aria-label="social.name"
          target="_blank"
          rel="noopener noreferrer"
          class="transition-transform duration-300 hover:-translate-y-1"
        >
          <img
            :src="social.icon"
            :alt="social.name"
            class="h-8 w-8"
          />
        </a>
      </div>
    </div>

    <img
        :src="FooterImage"
        alt=""
    />
        
  </footer>
</template>