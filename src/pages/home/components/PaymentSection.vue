<script setup lang="ts">
import PaymentMachine from "@/assets/images/payment-machine.svg";
import PaymentVector from "@/assets/images/payment-vector.svg";
import BaseButton from "@/components/ui/BaseButton.vue";
import ArrowIcon from "@/assets/images/arrow.svg";

</script>

<template>
    <div class="app-container relative my-20">
  <div class="flex flex-col-reverse lg:grid lg:grid-cols-2">
    <!-- Image -->
    <img
      :src="PaymentMachine"
      alt="Payment machine image"
      class="w-full rounded-4xl mt-6"
    />

    <!-- Card -->
    <div
      class="z-10 rounded-3xl bg-brand p-8 text-white md:p-10 lg:absolute lg:-bottom-20 lg:left-1/2 lg:w-[45%] lg:-translate-x-1/2"
    >
      <h2 class="mb-4 text-3xl font-bold leading-tight md:text-4xl">
        Ready to cross over to<br />
        <span class="text-secondary">better payments?</span>
      </h2>

      <p class="mb-8 text-lg text-gray-300">
        Get set up in minutes. No hidden fees,<br />
        no long contracts.
      </p>

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

    <!-- Vector -->
    <img
      :src="PaymentVector"
      alt=""
      class="hidden lg:col-start-2 lg:block"
    />
  </div>
</div>
</template>