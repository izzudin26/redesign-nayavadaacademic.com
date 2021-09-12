<template>
  <div
    id="paketKursus"
    class="
      flex flex-col
      bg-blue-100
      w-full
      justify-center
      space-y-12
      items-center
      px-5
      py-10
    "
  >
    <div class="flex flex-col w-auto space-y-1">
      <div class="text-3xl font-semibold">Paket Kursus</div>
      <div class="bg-blue-600 rounded-full h-1 w-full"></div>
    </div>
    <div
      class="
        grid
        md:grid-cols-2
        lg:grid-cols-4
        grid-cols-1 grid-flow-row grid-rows-2
        gap-16
        px-10
        container
        w-full
        md:w-full
        items-stretch
        justify-center
      "
    >
      <div
        v-for="(kursus, i) in paketKursus"
        :key="i"
        class="
          bg-white
          shadow-lg
          p-5
          rounded-xl
          flex flex-col
          text-center
          space-y-5
          col-span-1
          transform
          transition-all
          hover:scale-105
          duration-300
          hover:text-blue-600
        "
      >
        <span class="text-xl font-semibold">{{ kursus.type }}</span>
        <span class="text-xl font-semibold">
          IDR
          <span class="text-3xl font-bold">{{ kursus.price }}K</span>
        </span>
        <span class="text-lg font-semibold px-3 mx-auto text-center">{{
          kursus.name
        }}</span>
        <div>
          Materi:
          <div class="mt-3 space-y-2 flex flex-col">
            <ul class="list-disc px-10">
              <li
                class="text-left mx-auto font-semibold"
                v-for="(materi, materiIndex) in kursus.materi"
                :key="materiIndex"
              >
                {{ materi }}
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { paketKursus } from "./data";

export default {
  name: "PaketKursus",
  data: () => ({
    paketKursus,
  }),
};
</script>

<style></style>
