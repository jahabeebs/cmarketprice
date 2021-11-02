<template>
  <div class="h-screen bg-gradient-to-b from-blue-900 to-gray-700 overflow-auto">
    <h1 class="flex justify-center text-white text-center text-5xl md:text-6xl font-bold">Commodity Market
      Prices</h1>
    <h2 class="flex justify-center text-white text-center italic text-xs mt-2 md:mt-2 md:text-lg font-bold">Monthly
      agricultural commodity prices using World Bank data</h2>
    <div class="flex md:mt-8 mt-2 justify-center">
    </div>
    <NuxtLink to="/bananas">
      <CommodityCard imageName="bananas" commodity="Bananas"/>
    </NuxtLink>
    <NuxtLink to="/barley">
      <CommodityCard imageName="barley" commodity="Barley"/>
    </NuxtLink>
    <NuxtLink to="/cocoa">
      <CommodityCard imageName="cocoa" commodity="Cocoa"/>
    </NuxtLink>
    <NuxtLink to="/coffeearabica">
      <CommodityCard imageName="beans" commodity="Coffee (Arabicas)"/>
    </NuxtLink>
    <NuxtLink to="/coffeerobusta">
      <CommodityCard imageName="beans" commodity="Coffee (Robustas)"/>
    </NuxtLink>
    <NuxtLink to="/maize">
      <CommodityCard imageName="maize" commodity="Maize"/>
    </NuxtLink>
    <NuxtLink to="/oranges">
      <CommodityCard imageName="oranges" commodity="Oranges"/>
    </NuxtLink>
    <NuxtLink to="/palmoil">
      <CommodityCard imageName="palmoil" commodity="Palm Oil"/>
    </NuxtLink>
    <NuxtLink to="/soybeans">
      <CommodityCard imageName="soybeans" commodity="Soybeans"/>
    </NuxtLink>
    <NuxtLink to="/sugar">
      <CommodityCard imageName="sugar" commodity="Sugar"/>
    </NuxtLink>
    <NuxtLink to="/tea">
      <CommodityCard imageName="tea" commodity="Tea"/>
    </NuxtLink>
    <NuxtLink to="/wheat">
      <CommodityCard imageName="wheat" commodity="Wheat"/>
    </NuxtLink>
    <p class="align-middle text-xs md:text-sm text-white text-center italic mt-24 sm:mt-12"> This site is only
      for
      informational purposes <br> Accuracy of the prices is not guaranteed <br> Built by Jacob Habib (@jahabeebs)
      <br>
      Favicon is attributed to the Twemoji project</p>
  </div>
</template>
