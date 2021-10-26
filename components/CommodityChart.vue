<script>
import {Line} from 'vue-chartjs'

export default {
  extends: Line,
  props: {
    chartData: {
      type: Array | Object,
      required: false,
      default: null
    },
    chartLabels: {
      type: Array,
      required: true
    },
    labelOfCommodity: {
      type: String,
      required: true
    }
  },
  mounted() {
    this.renderChart({
      labels: this.chartLabels,
      datasets: [
        {
          label: this.labelOfCommodity,
          borderColor: '#249EBF',
          pointBackgroundColor: 'white',
          borderWidth: 1,
          pointBorderColor: '#249EBF',
          backgroundColor: 'transparent',
          data: this.chartData
        }
      ]
    }, this.options)
  }
}
</script>
