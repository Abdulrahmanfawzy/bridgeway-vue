<script setup lang="ts">
import PaymentIcon from "@/assets/images/payment.svg";
import PayoutIcon from "@/assets/images/payouts.svg";
import ReconcileIcon from "@/assets/images/recon.svg";
import ReportIcon from "@/assets/images/report.svg";
import SecureIcon from "@/assets/images/secure.svg";
import DevIcon from "@/assets/images/dev.svg";

const features = [
  {
    title: 'Accept Payments',
    description: 'Take cards, wallets, and bank transfers online and in person through a single integration.',
    icon: PaymentIcon,
    cardStyle: "bg-brand",
    iconStyle: "bg-secondary",
    textStyle: "text-white"
  },
  {
    title: 'Reconcile automatically',
    description: 'Every transaction is matched to your books in real time, so month-end stops being a chore.',
    icon: ReconcileIcon,
    cardStyle: "bg-white border-2 border-gray-200",
    iconStyle: "bg-brand",
    textStyle: "text-brand"
  },
  {
    title: 'Send Payouts',
    description: 'Pay suppliers, partners, and staff in minutes, in bulk or one at a time.',
    icon: PayoutIcon,
    cardStyle: "bg-brand",
    iconStyle: "bg-secondary",
    textStyle: "text-white"
  },
  {
    title: 'Secure by default',
    description: 'Built-in fraud checks, encryption, and identity verification protect every payment.',
    icon: SecureIcon,
    cardStyle: "bg-white border-2 border-gray-200",
    iconStyle: "bg-brand",
    textStyle: "text-brand"
  },
  {
    title: 'Clear reporting',
    description: 'Live dashboards show where your money is, what\'s settled, and what\'s pending.',
    icon: ReportIcon,
    cardStyle: "bg-brand",
    iconStyle: "bg-secondary",
    textStyle: "text-white"
  },
  {
    title: 'Built for developers',
    description: 'Clean APIs, sandbox testing, and webhooks help your team ship in days, not months.',
    icon: DevIcon,
    cardStyle: "bg-white border-2 border-gray-200",
    iconStyle: "bg-brand",
    textStyle: "text-brand"
  }
]


</script>

<template>
    <div class="app-container mb-10">

        <section class="lg:flex justify-between gap-2 mb-10 lg:mb-20">
            <h2 class="text-4xl lg:text-6xl font-extrabold text-brand mb-5 lg:mb-0">
                Everything payments, <br>
                on one bridge
            </h2>
            <p class="text-xl lg:text-3xl">
                One platform connects you to customers, <br class="hidden lg:block"> banks, and your own books, so money <br class="hidden lg:block"> moves without the friction.
            </p>
        </section>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-5">
            <div
                v-for="feature in features"
                :key="feature.title"
                :class="[feature.cardStyle, feature.textStyle]"
                class="rounded-2xl p-8"
            >
                <div
                :class="feature.iconStyle"
                class="mb-6 flex h-14 w-14 items-center justify-center rounded-xl"
                >
                <img :src="feature.icon" :alt="feature.title" class="h-7 w-7" />
                </div>

                <h3 class="mb-3 text-2xl font-bold">
                {{ feature.title }}
                </h3>

                <p>{{ feature.description }}</p>
            </div>
        </div>
    </div>
</template>