<template>
  <div class="h-screen bg-gray-900 overflow-auto">
    <h1 class="flex justify-center text-white text-center text-5xl md:text-6xl sm:text-3xl font-bold">Commodity Market
      Prices</h1>
    <div class="flex mt-12 justify-center">
    </div>
    <NuxtLink to="/bananas">
      <CommodityCard imageName="bananas" commodity="Bananas"/>
    </NuxtLink>
    <NuxtLink to="/barley">
      <CommodityCard imageName="barley" commodity="Barley"/>
    </NuxtLink>
    <NuxtLink to="/coffeearabica">
      <CommodityCard imageName="beans" commodity="Coffee (Arabicas)"/>
    </NuxtLink>
    <NuxtLink to="/coffeerobusta">
      <CommodityCard imageName="beans" commodity="Coffee (Robustas)"/>
    </NuxtLink>
    <NuxtLink to="/palmoil">
      <CommodityCard imageName="palmoil" commodity="Palm Oil"/>
    </NuxtLink>
    <p class="align-middle text-xs md:text-sm text-white text-center italic mt-24 sm:mt-12"> This site is only
      for
      informational purposes <br> Accuracy of the prices is not guaranteed <br> Built by Jacob Habib (@jahabeebs)
      <br>
      Favicon is attributed to the Twemoji project</p>
  </div>
</template>
<script>

</script>
<!-- <CommodityCard commodity = "Steel" />
<CommodityCard commodity = "Coal" />
<CommodityCard commodity = "Crude Oil" />
<CommodityCard commodity = "Natural Gas" />
<CommodityCard commodity = "Cocoa" />
<CommodityCard commodity = "Tea" />
<CommodityCard commodity = "Palm Oil" />
<CommodityCard commodity = "Soybeans" />
<CommodityCard commodity = "Soybean Oil" />
<CommodityCard commodity = "Barley" />
<CommodityCard commodity = "Maize" />
<CommodityCard commodity = "Rice" />
<CommodityCard commodity = "Wheat" />
<CommodityCard commodity = "Oranges" />
<CommodityCard commodity = "Sugar" />
<CommodityCard commodity = "Cotton" />
<CommodityCard commodity = "Rubber" />
<CommodityCard commodity = "Aluminum" />
<CommodityCard commodity = "Iron" />
<CommodityCard commodity = "Lead" />
<CommodityCard commodity = "Gold" />
<CommodityCard commodity = "Silver" />

<p class="align-middle text-xs md:text-sm text-white text-center italic fixed inset-x-0 bottom-0"> This site is only for
  informational purposes <br> Accuracy of the prices is not guaranteed <br> Built by Jacob Habib (@jahabeebs)
  <br>
  Favicon is attributed to the Twemoji project</p>
</div>
</div>
</template>
