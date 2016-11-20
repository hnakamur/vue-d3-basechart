<template>
  <svg></svg>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  props: ['chartData'],
  methods: {
    renderChart () {
      throw new Error('Please implement renderChart method in subclass of BaseChart.')
    }
  },
  mounted () {
    this.renderChart()
  },
  watch: {
    chartData: {
      handler: 'renderChart',
      deep: true
    }
  }
})
</script>
