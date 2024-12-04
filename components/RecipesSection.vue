<script lang="ts" setup>
import { type RecipeResponse } from "~/types/types";
const { data, error } = await useFetch<RecipeResponse>(
  "https://dummyjson.com/recipes?limit=12"
);
</script>

<template>
  <section class="py-20 px-12">
    <h2 class="text-3xl lg:text-5xl mb-2">Discover, Create, Share</h2>
    <p class="text-lg lg:text-xl mb-8">Check out our most popular recipes!</p>
    <div
      v-if="!error"
      class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-4 gap-y-8"
    >
      <RecipeCard v-for="recipe in data?.recipes" :recipe="recipe" />
    </div>
    <p v-else class="text-xl">
      Opps, something went wrong. Please try again later
    </p>
  </section>
</template>

<style scoped></style>
