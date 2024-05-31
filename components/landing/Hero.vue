<script setup>
import { onMounted, ref } from 'vue';
import { gsap } from 'gsap';

const title = ref(null);

onMounted(() => {
  const letters = title.value.textContent.split("").map(char => `<span class="letter">${char}</span>`).join("");
  title.value.innerHTML = letters;

  const letterEls = title.value.querySelectorAll('.letter');
  gsap.fromTo(
      letterEls,
      { rotation: 360, opacity: 0 },
      { rotation: 0, opacity: 1, duration: .8, stagger: 0.1, ease: "back.out(1.7)" }
  );
});
</script>


<template>
  <main class="grid lg:grid-cols-2 place-items-center md:pt-16 pb-8 md:pt-8">
    <div class="p-8 md:p-24 md:order-1 md:block">
      <img
        class="rounded-full transition-transform transform hover:scale-125"
        src="~/assets/img/hero.jpg"
        alt="Starship starts the engine"
        loading="eager"
        format="avif"
        width="512"
        height="512"
      />
    </div>

    <div>
      <h1 class="text-5xl lg:text-6xl xl:text-7xl font-bold lg:tracking-tight animated-title" ref="title">
        Easier than ever: website deployment
      </h1>
      <p class="text-lg mt-4 text-slate-600 max-w-xl">
        From code to hosting in just a few clicks
      </p>
      <div class="mt-6 flex flex-col sm:flex-row gap-3">
        <LandingLink
          href="/before"
          rel="noopener"
          >Go to Before</LandingLink
        >
        <LandingLink
          size="lg"
          styleName="outline"
          rel="noopener"
          href="/after"
          >View Our solution</LandingLink
        >
      </div>
    </div>
  </main>
</template>


<style scoped>
.animated-title {
  position: relative;
  text-align: center;
  font-size: 2rem;
  margin-top: 1rem;
}

.letter {
  display: inline-block;
}
</style>