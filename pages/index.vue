<script lang="ts" setup>
useSeoMeta({
  title: "Nuxtcipes",
  description: "Recipes for you to cook!",
  ogTitle: "Nuxtcipes",
  ogDescription: "Recipes for you to cook!",
  ogImage: "/nuxt-course-hero.png",
  ogUrl: `http:localhost:3000`,
  twitterTitle: "Nuxtcipes",
  twitterDescription: "Recipes for you to cook!",
  twitterImage: "nuxt-course-hero.png",
  twitterCard: "summary",
});
</script>

<template>
  <main>
    <section class="bg-[#f1f1f1] px-12">
      <div
        class="container flex flex-col lg:flex-row items-center py-20 gap-10 mx-auto"
      >
        <div class="flex-1 order-2 lg:order-1 text-center lg:text-left">
          <h1 class="text-3xl lg:text-5xl font-extrabold mb-6 text-balance">
            Master the Kitchen with Ease: Unleash Your Inner Chef Today!
          </h1>
          <p class="text-lg lg:text-2xl mb-8 text-balance">
            Discover recipes helping you to find the easiest way to cook.
          </p>
          <NuxtLink
            to="/recipes"
            class="px-4 py-3 text-white self-start bg-dodgeroll-gold rounded-md text-lg cursor-pointer bg-orange-600"
          >
            Browse Recipes
          </NuxtLink>
        </div>
        <div class="flex-1 order-1 lg:order-2">
          <NuxtImg
            sizes="xs:100vw sm:667px"
            src="/nuxt-course-hero.png"
            format="webp"
            densities="x1"
            alt=""
          />
        </div>
      </div>
    </section>
    <RecipesSection />
  </main>
</template>

<style></style>
