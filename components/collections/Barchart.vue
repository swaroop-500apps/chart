<template>
    <Bar id="mychartid" />
</template>
  
<script setup>
 import {onMounted, ref , defineProps } from 'vue';
 import VueHighCharts from 'vue3-highcharts'
 const mychartid = ref(null);
 let BarInstance = null;
 const props = defineProps({
    options: {
      type: Boolean,
      required: true,
    },
    data: {
      type: Object,
      required: true,
    },
  });
  onMounted(() => {
    const Bar = mychartid.value;
    BarInstance = new Chart(Bar, {
      type: 'Grid Chart',
      data: props.data,
      options:props.data,
    });
  });
</script>
