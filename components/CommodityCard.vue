<template>
  <div class="flex flex-col items-center justify-center">
    <div class="grid mt-12 md:mt-10 md:gap-8">
      <div class="flex">
        <div
          class="
            bg-white
            shadow-md
            rounded-3xl
            p-4
            transitions
            duration-500
            ease-in-out
            transform
            hover: translate-y-1
            hover: scale-110
          "
        >
          <div class="flex align-middle">
            <div class="flex-col justify-evenly">
              <div class="flex flex-row gap-2">
                <img
                  src="~/assets/beans.svg"
                  class="
                  h-16
                  object-scale-down
                  md:object-cover
                  md:w-full
                  md:h-24
                  rounded-2xl
                "
                />
                <div class="flex md:pt-7 text-4xl pt-3 font-small font-black">{{ commodity }}</div>
              </div>
              <p class="mt-3"></p>
              <div class="flex border-t border-gray-200"></div>
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
