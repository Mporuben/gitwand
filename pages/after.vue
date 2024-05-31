<script setup>
definePageMeta({
  layout: "landing",
});
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>Our solution</template>
      <template v-slot:desc>Now to deploy the web, need to take two steps</template>
    </LandingSectionhead>
    <div class="flex flex-row justify-center mt-16">
      <img
          class="rounded-md"
          src="/assets/img/wow.gif"
          alt="sad man"
          loading="eager"
          format="avif"
          width="600"
          height="512"
      />
    </div>

      <div class="mt-16 grid lg:grid-cols-2 place-items-center mx-auto max-w-4xl">
        <div class="">
          <p class="text-xl text-center mb-4">1. Code change</p>
        </div>
        <div class="mb-8">
          <img
              class="rounded-md"
              src="/assets/img/typing-cat.gif"
              alt="sad man"
              loading="eager"
              format="avif"
              width="400"
              height="400"
          />
        </div>
          <div class="order-last">
            <img
                class="rounded-md"
                src="/assets/img/git-push2.jpg"
                alt="sad man"
                loading="eager"
                format="avif"
                width="400"
                height="400"
            />
          </div>
        <div>
            <p class="text-xl text-center mb-4">2. Git push</p>
          </div>
        </div>
    <div class="flex flex-col items-center justify-center mt-16 mb-24">
      <p class="text-xl mb-4">And thats it! 🎉</p>
      <img
          class="rounded-md"
          src="/assets/img/happy.gif"
          alt="sad man"
          loading="eager"
          format="avif"
          width="300"
          height="300"
      />
    </div>
  </LandingContainer>
</template>
