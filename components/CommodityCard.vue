<template>
  <div class="flex flex-row justify-center">
    <div class="mt-6 md:mt-8">
      <div
        class="
            bg-white
            shadow-md
            md:rounded-3xl
            rounded-2xl
            p-2
            duration-500
            ease-in-out
            transform
            hover: translate-y-1
            hover: scale-110
          "
      >
        <div>
          <div class="justify-evenly">
            <div class="flex gap-2">
              <img
                :src="imageSource"
                class="
                  md:h-24
                  h-12
                  md:object-cover
                  md:w-full
                  rounded-2xl
                "
              />
              <div class="md:text-3xl text-lg font-small font-black m-auto">{{ commodity }}</div>
            </div>
            <p class="mt-2"></p>
            <div class="border-t border-gray-200"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    commodity: String,
    imageName: String
  },
  computed: {
    imageSource() {
      return require(`~/assets/${this.imageName}.svg`)
    }
  }
};
</script>
