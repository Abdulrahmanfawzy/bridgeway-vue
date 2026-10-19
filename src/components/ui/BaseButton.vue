<script setup lang="ts">
withDefaults(
  defineProps<{
    label: string;
    variant?: "primary" | "secondary";
    type?: "button" | "submit" | "reset";
  }>(),
  {
    variant: "primary",
    type: "button",
  }
);

defineEmits<{
  click: [event: MouseEvent];
}>();
</script>

<template>
  <button
    :type="type"
    :class="[
      'inline-flex items-center justify-center gap-2 rounded-full px-6 py-3 font-medium transition-all duration-300 hover:-translate-y-0.5',
      variant === 'primary'
        ? 'bg-secondary text-brand hover:opacity-90'
        : 'border border-white/30 text-white hover:bg-white/10',
    ]"
    @click="$emit('click', $event)"
  >
    <span>{{ label }}</span>

    <slot name="icon" />
  </button>
</template>