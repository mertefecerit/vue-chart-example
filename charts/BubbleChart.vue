<template>
    <Bubble :chart-options="chartOptions"
         :chart-data="chartData"
         :chart-id="chartId"
         :plugins="plugins"
         :css-classes="cssClasses"
         :styles="styles"
         :width="width"
         :height="height">
    </Bubble>
</template>

<script>
import { Bubble } from 'vue-chartjs'

import {
    Chart as ChartJS,
    Title,
    Tooltip,
    Legend,
    PointElement,
    LinearScale,
    Plugin
} from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, PointElement, LinearScale)
export default {
    name: "BubbleChart",
    components:{
        Bubble
    },
    props:{
        chartId: {
            type: String,
            default: 'bubble-chart'
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
}
</script>

<style scoped>

</style>
