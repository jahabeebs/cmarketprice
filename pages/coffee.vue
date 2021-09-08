<template>
  <div>
  <client-only>
    <line-chart :data="chartData" :styles="myStyles"></line-chart>
  </client-only>
  </div>
</template>
<script>
export default {
  data() {
    return {
      height: 20,
      chartData: {
        datasets: [{
          label: 'Title',
          data: [45, 55, 48, 35, 12]
        }]
      }
    };
  },
  computed: {
    myStyles() {
      return {
        height: `${this.height}px`,
        position: 'relative'
      }
    }
  },
}
</script>
