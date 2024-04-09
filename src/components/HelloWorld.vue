<template>
  <div id="sdg-chart"></div>
</template>

<script setup>
import { onMounted } from 'vue';
import Highcharts from 'highcharts';

onMounted(() => {
  const chartOptions = {
    chart: {
      type: 'column',
      renderTo: 'sdg-chart'
    },
    title: {
      text: 'Company Contributions to UN SDGs'
    },
    xAxis: {
      categories: ['HighSoft', 'TV2', 'Sparebanken Vest']
    },
    yAxis: {
      min: 0,
      title: {
        text: 'Contribution Level'
      },
      stackLabels: {
        enabled: true
      }
    },
    tooltip: {
      shared: true
    },
    plotOptions: {
      column: {
        stacking: 'normal'
      }
    },
    series: [
      { name: 'SDG 1: No Poverty', data: [5, null, 4], color: '#EB1C2D' },
      { name: 'SDG 2: Zero Hunger', data: [2, 2, null], color: '#D3A029' },
      { name: 'SDG 3: Good Health and Well-being', data: [3, 4, null], color: '#279B48' },
      { name: 'SDG 4: Quality Education', data: [null, 3, 2], color: '#C31F33' },
      { name: 'SDG 5: Gender Equality', data: [null, null, 4], color: '#EF402D' },
      { name: 'SDG 6: Clean Water and Sanitation', data: [3, null, 4], color: '#00AED9' },
      { name: 'SDG 7: Affordable and Clean Energy', data: [null, 2, 2], color: '#FDB713' },
      { name: 'SDG 8: Decent Work and Economic Growth', data: [3, 4, null], color: '#8F1838' },
      { name: 'SDG 9: Industry, Innovation, and Infrastructure', data: [null, null, 2], color: '#F36D26' },
      { name: 'SDG 10: Reduced Inequalities', data: [2, 2, null], color: '#E11484' },
      { name: 'SDG 11: Sustainable Cities and Communities', data: [null, 4, 2], color: '#F99D26' },
      { name: 'SDG 12: Responsible Consumption and Production', data: [3, null, null], color: '#CF8D2A' },
      { name: 'SDG 13: Climate Action', data: [null, null, 4], color: '#48773D' },
      { name: 'SDG 14: Life Below Water', data: [2, 2, null], color: '#007DBC' },
      { name: 'SDG 15: Life on Land', data: [null, 3, 4], color: '#3EB049' },
      { name: 'SDG 16: Peace, Justice, and Strong Institutions', data: [3, null, null], color: '#02558B' },
      { name: 'SDG 17: Partnerships for the Goals', data: [null, 2, 2], color: '#183668' }
    ]

  };

  Highcharts.chart(chartOptions);
});
</script>

<style>
#sdg-chart {
  width: 100%;
  height: 600px; /* Adjust height as needed */
}
</style>





