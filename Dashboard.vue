<template>
    <Layout>
        <Head title="Dashboard"></Head>
        <AppHeader title="Dashboard"></AppHeader>
        <div class="container">
            <div class="row">
                <div class="col-lg-12 p-0">
                    <div class="p-2 bg-white shadow-sm rounded">
                        <div class="row">
                            <div class="col-lg-4">
                                <BarChart
                                    :chartData="barChartData"
                                    :chartOptions="barChartConfig">
                                </BarChart>
                            </div>
                            <div class="col-lg-4">
                                <BubbleChart :chartData="bubbleChartData"
                                             :chartOptions="chartBubbleConfig">
                                </BubbleChart>
                            </div>
                            <div class="col-lg-4">
                                <DoughnutChart :chartData="doughnutChartData"
                                             :chartOptions="doughnutBubbleConfig">
                                </DoughnutChart>
                            </div>
                        </div>
                        <hr>
                        <div class="row">
                            <div class="col-lg-4">
                                <LineChart :chartData="lineChartData"
                                           :chartOptions="lineChartConfig">
                                </LineChart>
                            </div>
                            <div class="col-lg-4">
                                <PieChart :chartData="pieChartData"
                                           :chartOptions="pieChartConfig">
                                </PieChart>
                            </div>
                            <div class="col-lg-4">
                                <PolarAreaChart :chartData="polarAreaChartData"
                                                :chartOptions="polarAreaChartConfig">
                                </PolarAreaChart>
                            </div>
                        </div>
                        <hr>
                        <div class="row">
                            <div class="col-lg-4">
                                <RadarChart :chartData="radarChartData"
                                            :chartOptions="radarChartConfig">
                                </RadarChart>
                            </div>
                            <div class="col-lg-4">
                                <ScatterChart :chartData="scatterChartData"
                                              :chartOptions="scatterChartConfig">
                                </ScatterChart>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </Layout>
</template>

<script>
import Layout from "../Layout";
import { Head } from '@inertiajs/inertia-vue3'
import AppHeader from "../Components/AppHeader";
import BarChart from "../Components/charts/BarChart";
import BubbleChart from "../Components/charts/BubbleChart";
import DoughnutChart from "../Components/charts/DoughnutChart";
import LineChart from "../Components/charts/LineChart";
import PieChart from "../Components/charts/PieChart";
import PolarAreaChart from "../Components/charts/PolarAreaChart";
import RadarChart from "../Components/charts/RadarChart";
import ScatterChart from "../Components/charts/ScatterChart";

export default {
    name: "app",
    components:{
        Layout,
        Head,
        AppHeader,
        BarChart,
        BubbleChart,
        DoughnutChart,
        LineChart,
        PieChart,
        PolarAreaChart,
        RadarChart,
        ScatterChart,
    },
    setup(){
        // Bar Chart
        const barChartData = {
            'labels': [
                'January',
                'February',
                'March',
                'April',
                'May',
                'June',
                'July',
                'August',
                'September',
                'October',
                'November',
                'December'
            ],
            datasets: [
                {
                    fill: false,
                    label: 'Data One',
                    backgroundColor: '#2ecc71',
                    data: [40, 20, 12, 39, 10, 40, 39, 80, 40, 20, 12, 11]
                }
            ]

        }
        const barChartConfig = {
            responsive: true,
        }
        // Bar Chart



        // Bubble Chart
        const bubbleChartData = {
            datasets: [
                {
                    label: 'Data One',
                    backgroundColor: '#f87979',
                    data: [
                        {
                            x: 20,
                            y: 25,
                            r: 5
                        },
                        {
                            x: 40,
                            y: 10,
                            r: 10
                        },
                        {
                            x: 30,
                            y: 22,
                            r: 30
                        }
                    ]
                },
                {
                    label: 'Data Two',
                    backgroundColor: '#7C8CF8',
                    data: [
                        {
                            x: 10,
                            y: 30,
                            r: 15
                        },
                        {
                            x: 20,
                            y: 20,
                            r: 10
                        },
                        {
                            x: 15,
                            y: 8,
                            r: 30
                        }
                    ]
                }
            ]
        }
        const chartBubbleConfig = {
            responsive: true,
        }
        // Bubble Chart



        // Doughnut Chart
        const doughnutChartData = {
            labels: ['VueJs', 'EmberJs', 'ReactJs', 'AngularJs'],
            datasets: [
                {
                    backgroundColor: ['#41B883', '#E46651', '#00D8FF', '#DD1B16'],
                    data: [40, 20, 80, 10]
                }
            ]
        }
        const doughnutBubbleConfig = {
            responsive: true,
        }
        // Doughnut Chart



        // Line Chart
        const lineChartData = {
            labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
            datasets: [
                {
                    label: 'Data One',
                    backgroundColor: '#f87979',
                    data: [40, 39, 10, 40, 39, 80, 40]
                }
            ]
        }
        const lineChartConfig = {
            responsive: true,
        }
        // Line Chart



        // Pie Chart
        const pieChartData = {
            labels: ['VueJs', 'EmberJs', 'ReactJs', 'AngularJs'],
            datasets: [
                {
                    backgroundColor: ['#41B883', '#E46651', '#00D8FF', '#DD1B16'],
                    data: [40, 20, 80, 10]
                }
            ]
        }
        const pieChartConfig = {
            responsive: true,
        }
        // Pie Chart



        // PolarArea Chart
        const polarAreaChartData = {
            labels: [
                'Eating',
                'Drinking',
                'Sleeping',
                'Designing',
                'Coding',
                'Cycling',
                'Running'
            ],
            datasets: [
                {
                    label: 'My First dataset',
                    backgroundColor: 'rgba(179,181,198,0.2)',
                    pointBackgroundColor: 'rgba(179,181,198,1)',
                    pointBorderColor: '#fff',
                    pointHoverBackgroundColor: '#fff',
                    pointHoverBorderColor: 'rgba(179,181,198,1)',
                    data: [65, 59, 90, 81, 56, 55, 40]
                },
                {
                    label: 'My Second dataset',
                    backgroundColor: 'rgba(255,99,132,0.2)',
                    pointBackgroundColor: 'rgba(255,99,132,1)',
                    pointBorderColor: '#fff',
                    pointHoverBackgroundColor: '#fff',
                    pointHoverBorderColor: 'rgba(255,99,132,1)',
                    data: [28, 48, 40, 19, 96, 27, 100]
                }
            ]
        }
        const polarAreaChartConfig = {
            responsive: true,
        }
        // PolarArea Chart



        // PolarArea Chart
        const radarChartData = {
            labels: [
                'Eating',
                'Drinking',
                'Sleeping',
                'Designing',
                'Coding',
                'Cycling',
                'Running'
            ],
            datasets: [
                {
                    label: 'My First dataset',
                    backgroundColor: 'rgba(179,181,198,0.2)',
                    borderColor: 'rgba(179,181,198,1)',
                    pointBackgroundColor: 'rgba(179,181,198,1)',
                    pointBorderColor: '#fff',
                    pointHoverBackgroundColor: '#fff',
                    pointHoverBorderColor: 'rgba(179,181,198,1)',
                    data: [65, 59, 90, 81, 56, 55, 40]
                },
                {
                    label: 'My Second dataset',
                    backgroundColor: 'rgba(255,99,132,0.2)',
                    borderColor: 'rgba(255,99,132,1)',
                    pointBackgroundColor: 'rgba(255,99,132,1)',
                    pointBorderColor: '#fff',
                    pointHoverBackgroundColor: '#fff',
                    pointHoverBorderColor: 'rgba(255,99,132,1)',
                    data: [28, 48, 40, 19, 96, 27, 100]
                }
            ]
        }
        const radarChartConfig = {
            responsive: true,
        }
        // PolarArea Chart



        // PolarArea Chart
        const scatterChartData = {
            datasets: [
                {
                    label: 'Scatter Dataset 1',
                    fill: false,
                    borderColor: '#f87979',
                    backgroundColor: '#f87979',
                    data: [
                        {
                            x: -2,
                            y: 4
                        },
                        {
                            x: -1,
                            y: 1
                        },
                        {
                            x: 0,
                            y: 0
                        },
                        {
                            x: 1,
                            y: 1
                        },
                        {
                            x: 2,
                            y: 4
                        }
                    ]
                },
                {
                    label: 'Scatter Dataset 2',
                    fill: false,
                    borderColor: '#7acbf9',
                    backgroundColor: '#7acbf9',
                    data: [
                        {
                            x: -2,
                            y: -4
                        },
                        {
                            x: -1,
                            y: -1
                        },
                        {
                            x: 0,
                            y: 1
                        },
                        {
                            x: 1,
                            y: -1
                        },
                        {
                            x: 2,
                            y: -4
                        }
                    ]
                }
            ]
        }
        const scatterChartConfig = {
            responsive: true,
        }
        // PolarArea Chart


        return {
            barChartData,
            barChartConfig,

            chartBubbleConfig,
            bubbleChartData,

            doughnutChartData,
            doughnutBubbleConfig,

            lineChartData,
            lineChartConfig,

            pieChartData,
            pieChartConfig,

            polarAreaChartData,
            polarAreaChartConfig,

            radarChartData,
            radarChartConfig,

            scatterChartData,
            scatterChartConfig
        }
    }
}
</script>

<style scoped>

</style>
