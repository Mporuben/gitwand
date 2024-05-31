<script setup>
definePageMeta({
  layout: "landing",
});
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>Сurrent method of upload page</template>
    </LandingSectionhead>
    <LandingRainEffect />
    <div class="grid lg:grid-cols-2 mt-16 place-items-center pr-5 pl-5 lg:pr-0 lg:pl-0">
      <img
          class="rounded-md"
          src="../assets/img/image1.jpg"
          alt="sad man"
          loading="eager"
          format="avif"
          width="512"
          height="512"
      />
      <h3 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
        This is how a client feels when trying to upload a webpage
      </h3>
    </div>
    <div class="flex flex-col gap-3 mx-auto max-w-4xl mt-24 mb-24">
      <h3 class="text-2xl font-bold text-center mb-12">If you want to change something on your page:</h3>
      <div class="grid lg:grid-cols-2 place-items-center">
        <div class="m-2 font-medium text-lg">1. Code change</div>
        <div class="m-2">
          <img
          class="rounded-md"
          src="~/assets/img/change-code.gif"
          alt="Starship starts the engine"
          loading="eager"
          format="avif"
          width="512"
          height="512"
      />
        </div>
        <div class="m-2 font-medium text-lg lg:hidden">2. Git push</div>
        <div class="m-2">
          <img
            class="rounded-md"
            src="~/assets/img/git-push.png"
            alt="Starship starts the engine"
            loading="eager"
            format="avif"
            width="512"
            height="512"
        />
        </div>
        <div class="m-2 font-medium text-lg hidden lg:flex">2. Git push</div>
        <div class="m-2 font-medium text-lg">3. Npm run build</div>
        <div class="m-2">
          <img
            src="~/assets/img/npm-run-build.png"
            alt="Starship starts the engine"
            loading="eager"
            format="avif"
            width="512"
            height="512"
            class="rounded-md"
        />
          </div>
        <div class="mb-2 text-lg lg:hidden">
          4. Logging into FTP service (e.g., FileZilla)<br>
          5. Replacement of old files with the new ones.
        </div>
        <div class="m-2">
          <img
              src="~/assets/img/login-to-aftp.png"
              alt="Starship starts the engine"
              loading="eager"
              format="avif"
              width="512"
              height="512"
              class="rounded-md"
          />
        </div>
        <div class="m-2 font-medium flex flex-col items-center">
          <div class="mb-2 text-lg hidden lg:flex">
          4. Logging into FTP service (e.g., FileZilla)<br>
          5. Replacement of old files with the new ones.
          </div>

          <img
              src="~/assets/img/wtf.gif"
              alt="Starship starts the engine"
              loading="eager"
              format="avif"
              width="200"
              height="200"
              class="rounded"
          />
        </div>
      </div>
    </div>
  </LandingContainer>
</template>
