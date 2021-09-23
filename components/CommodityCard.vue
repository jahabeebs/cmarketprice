<template>
  <div class="relative flex flex-col items-center justify-center">
    <div class="grid mt-8 gap-8">
      <div class="flex flex-col">
        <div
          class="
            bg-white
            shadow-md
            rounded-3xl
            p-4
            transitionS
            duration-500
            ease-in-out
            transform
            hover:-translate-y-1
            hover:scale-110
          "
        >
          <div class="flex-none lg:flex">
            <div class="h-full w-full lg:h-24 lg:w-48 lg:mb-0 mb-3">
              <img
                src="~/assets/beans.svg"
                class="
                  w-full
                  object-scale-down
                  lg:object-cover
                  lg:h-24
                  rounded-2xl
                "
              />
            </div>
            <div class="flex-auto mt-5 ml-3 justify-evenly py-1">
              <div class="flex flex-wrap">
                <h2 class="flex-auto text-4xl font-medium">{{ commodity }}</h2>
              </div>
              <p class="mt-3"></p>

              <div class="flex p-4 pb-2 border-t border-gray-200"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["commodity"],
};
</script>
