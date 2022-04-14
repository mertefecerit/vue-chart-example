<template>
    <PolarArea :chart-options="chartOptions"
         :chart-data="chartData"
         :chart-id="chartId"
         :plugins="plugins"
         :css-classes="cssClasses"
         :styles="styles"
         :width="width"
         :height="height">
    </PolarArea>
</template>

<script>
import { PolarArea } from 'vue-chartjs'
import {
    Chart as ChartJS,
    Title,
    Tooltip,
    Legend,
    ArcElement,
    RadialLinearScale,
    Plugin
} from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, ArcElement, RadialLinearScale)

export default {
    name: "PolarAreaChart",
    props:{
        chartId: {
            type: String,
            default: 'polar-area-chart'
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
        PolarArea
    },
}
</script>

<style scoped>

</style>
