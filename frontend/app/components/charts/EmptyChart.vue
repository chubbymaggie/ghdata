<template>
  <div ref="chart" class="linechart"></div>
</template>


<script>

  import GHDataStats from '../../GHDataStats'
  import * as d3 from 'd3'

  export default {
    computed : {
      chart () {
        MG.data_graphic({
          title: "Missing Data",
          error: 'Data unavaliable',
          chart_type: 'missing-data',
          missing_text: 'Data could not be loaded',
          target: this.$refs.chart,
          full_width: true,
          height: 200
        });
      }
    }
  }

</script>