<template>
    <Scatter :chart-options="chartOptions"
         :chart-data="chartData"
         :chart-id="chartId"
         :plugins="plugins"
         :css-classes="cssClasses"
         :styles="styles"
         :width="width"
         :height="height">
    </Scatter>
</template>

<script>
import { Scatter } from 'vue-chartjs'
import {
    Chart as ChartJS,
    Title,
    Tooltip,
    Legend,
    LineElement,
    CategoryScale,
    LinearScale,
    PointElement,
    Plugin
} from 'chart.js'

ChartJS.register(
    Title,
    Tooltip,
    Legend,
    LineElement,
    CategoryScale,
    LinearScale,
    PointElement
)

export default {
    name: "ScatterChart",
    props:{
        chartId: {
            type: String,
            default: 'scatter-chart'
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
        Scatter
    },
}
</script>

<style scoped>

</style>
