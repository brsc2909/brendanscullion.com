<template>
    <client-only>
        <div class="my-5 mx-5 w-1/4 rounded-lg overflow-hidden">
            <figure>
                <v-chart class="w-auto h-44" :option="option" />
            </figure>
        </div>
    </client-only>
</template>

<script>
import { use } from "echarts/core";
import { CanvasRenderer } from "echarts/renderers";
import { CandlestickChart } from "echarts/charts";
import {
    TitleComponent,
    TooltipComponent,
    LegendComponent
} from "echarts/components";
import VChart, { THEME_KEY } from "vue-echarts";

use([
    CanvasRenderer,
    CandlestickChart,
    TitleComponent,
    TooltipComponent,
    LegendComponent
]);

export default defineComponent({
    name: "HelloWorld",
    components: {
        VChart
    },
    provide: {
        [THEME_KEY]: "dark"
    },
    setup() {
        const option = ref({
            title: {
                text: "Stock Prices",
                left: "center"
            },
            tooltip: {
                trigger: "item",
                formatter: "{a} <br/>{b} : {c} ({d}%)"
            },
            xAxis: {
                data: ['2017-10-24', '2017-10-25', '2017-10-26', '2017-10-27', '2017-10-28', '2017-10-29', '2017-10-30', '2017-10-31']
            },
            yAxis: {},
            series: [
                {
                    name: "Stock Prices",
                    type: "candlestick",
                    data: [
                        [20, 34, 10, 38],
                        [40, 35, 30, 50],
                        [31, 38, 33, 44],
                        [38, 15, 5, 42],
                        [20, 34, 10, 38],
                        [40, 35, 30, 50],
                        [31, 38, 33, 44],
                        [38, 15, 5, 42]
                    ],
                    emphasis: {
                        itemStyle: {
                            shadowBlur: 10,
                            shadowOffsetX: 0,
                            shadowColor: "rgba(0, 0, 0, 0.5)"
                        }
                    }
                }
            ]
        });

        return { option };
    }
});
</script>