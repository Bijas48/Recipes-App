<script setup lang="ts">
import type { NuxtError } from "#app";
import { Icon } from "@iconify/vue";

const props = defineProps({
  error: Object as () => NuxtError,
});
</script>

<template>
  <section class="flex min-h-screen flex-col items-center justify-center">
    <Icon icon="uil:exclamation-triangle" class="w-40 h-40 text-yellow-500" />
    <h1 class="mb-2 text-9xl font-bold">
      {{ error?.statusCode }}
    </h1>
    <p class="mb-10 text-xl sm:text-3xl">{{ error?.statusMessage }}</p>
    <NuxtLink
      to="/"
      class="px-4 py-2 text-white bg-dodgeroll-gold rounded-md text-lg cursor-pointer bg-orange-600"
    >
      Go home
    </NuxtLink>
  </section>
</template>
