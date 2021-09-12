<template>
  <div
    id="social"
    class="
      container
      flex flex-col
      p-10
      justify-center
      items-center
      text-center
      space-y-12
    "
  >
    <div class="flex flex-col w-auto space-y-1">
      <div class="text-3xl font-semibold">Tentang Saya</div>
      <div class="bg-blue-600 rounded-full h-1 w-full"></div>
    </div>
    <div
      class="
        grid grid-rows-2 grid-flow-row grid-cols-1
        md:grid-cols-2
        lg:grid-cols-3
        gap-5
        md:gap-10
        items-stretch
        w-full
        px-16
      "
    >
      <a
        v-for="(social, i) in social"
        :key="i"
        target="_blank"
        :href="social.direct"
      >
        <div
          class="
            shadow-lg
            p-3
            text-center
            rounded-lg
            col-span-1
            flex flex-row
            border-2 border-white
          "
          :class="social.style"
        >
          <img :src="social.icon" class="w-8" alt="" />
          <span class="mx-auto font-semibold">{{ social.label }}</span>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
import { social } from "./data";

export default {
  name: "Social",
  data: () => ({
    social,
  }),
};
</script>

<style></style>
