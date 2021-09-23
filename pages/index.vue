<template>
  <div class="h-screen bg-gray-900">
    <h1 class="text-white text-center text-5xl">Commodity Market Prices</h1>
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
      <p class="text-white text-center">The data displayed in this site is for informational purposes only. The accuracy of the prices is not
        guaranteed</p>
      <p class="text-white text-center italic">Built by Jacob Habib (jahabeebs on Twitter)</p>
      <p class="text-white text-center italic">Favicon is attributed to the Twemoji project</p>
    </div>
  </div>
</template>
