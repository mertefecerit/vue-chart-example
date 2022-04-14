<template>
    <Radar :chart-options="chartOptions"
         :chart-data="chartData"
         :chart-id="chartId"
         :plugins="plugins"
         :css-classes="cssClasses"
         :styles="styles"
         :width="width"
         :height="height">
    </Radar>
</template>

<script>
import { Radar } from 'vue-chartjs'
import {
    Chart as ChartJS,
    Title,
    Tooltip,
    Legend,
    PointElement,
    RadialLinearScale,
    LineElement,
    Plugin
} from 'chart.js'

ChartJS.register(
    Title,
    Tooltip,
    Legend,
    PointElement,
    RadialLinearScale,
    LineElement
)

export default {
    name: "RadarChart",
    props:{
        chartId: {
            type: String,
            default: 'radar-chart'
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
        Radar
    },
}
</script>

<style scoped>

</style>
