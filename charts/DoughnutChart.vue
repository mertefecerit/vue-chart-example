<template>
    <Doughnut :chart-options="chartOptions"
         :chart-data="chartData"
         :chart-id="chartId"
         :plugins="plugins"
         :css-classes="cssClasses"
         :styles="styles"
         :width="width"
         :height="height">
    </Doughnut>
</template>

<script>
import { Doughnut } from 'vue-chartjs'
import {
    Chart as ChartJS,
    Title,
    Tooltip,
    Legend,
    ArcElement,
    CategoryScale,
    Plugin
} from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, ArcElement, CategoryScale)

export default {
    name: "DoughnutChart",
    props:{
        chartId: {
            type: String,
            default: 'doughnut-chart'
        },
        width: {
            type: Number,
            default: 400
        },
        height: {
            type: Number,
            default: 400
        },
        cssClasses: {
            default: '',
            type: String
        },
        styles: {
            type: Object,
            default: () => {}
        },
        plugins: {
            type: Array,
            default: () => []
        },
        // Required fields But have default values - Begin
        chartData:{
            type: Object,
            default: () => {}
        },
        chartOptions: {
            type: Object,
            default: () => {}
        }
        // Required fields But have default values - End
    },
    components: {
        Doughnut
    },
}
</script>

<style scoped>

</style>
