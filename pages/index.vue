<template>
  <div class="h-screen bg-gray-900 overscroll-none">
    <h1 class="text-white text-center text-5xl md:text-6xl sm:text-3xl font-bold">Commodity Market Prices</h1>
    <div>
      <NuxtLink to="/coffee">
        <CommodityCard commodity="Coffee"/>
      </NuxtLink>
      <!-- <CommodityCard commodity = "Steel" />
    <CommodityCard commodity = "WTI crude (oil)" />
    <CommodityCard commodity = "Soybeans" />
    <CommodityCard commodity = "Iron" />
    <CommodityCard commodity = "Corn" />
    <CommodityCard commodity = "Gold" />
    <CommodityCard commodity = "Copper" />
    <CommodityCard commodity = "Aluminum" />
    <CommodityCard commodity = "Silver" />
    <CommodityCard commodity = "Brent crude oil" /> -->
      <p class="align-middle text-xs md:text-sm text-white text-center italic fixed inset-x-0 bottom-0"> This site is only for
        informational purposes <br> Accuracy of the prices is not guaranteed <br> Built by Jacob Habib (@jahabeebs)
        <br>
        Favicon is attributed to the Twemoji project</p>
    </div>
  </div>
</template>
