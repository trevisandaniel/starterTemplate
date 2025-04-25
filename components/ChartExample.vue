<!-- <template>
  <div>
    
  </div>
</template>

<script lang="ts" setup>

</script>

<style>

</style> -->
<template>
  <div class="bg-white p-4 shadow rounded mb-6">
    <h2 class="text-lg font-bold mb-2">Gráfico de Linhas</h2>
    <client-only>
      <apexchart type="line" height="300" :options="chartOptions" :series="series"></apexchart>
    </client-only>
  </div>
</template>

<script setup>
import VueApexCharts from 'vue3-apexcharts'
const series = [{ name: 'Vendas', data: [10, 41, 35, 51, 49, 62] }]
const chartOptions = {
  chart: { id: 'basic-line' },
  xaxis: { categories: ['Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun'] }
}
</script>

<script>
export default {
  components: { apexchart: VueApexCharts }
}
</script>
