<script setup>
definePageMeta({
    layout: "default",
    name: "Charts"
})

</script>
<template>
    <div class="flex flex-row">
        <BarChart />
        <CandleChart />
        <BarChart />
        <CandleChart />
        <BarChart />
        <CandleChart />
    </div>
</template>