<template>
  <collectionsBarchart :options="chartOptions" :data="chartData" />
</template>
  
<script setup>
import { ref, defineProps, defineEmits } from vue
import { Bar } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)

const chartData = {
  labels: ['January', 'February', 'March'],
  datasets: [{ data: [40, 20, 12] }]
}
  
const chartOptions = true

</script>