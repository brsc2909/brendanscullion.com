<template>
    <div class="bg-white h-auto p-10">
        <h1>Hello Test</h1>
        <div>Number: {{ number }}</div>
        <button @click="increment"
            class="border rounded-xl px-2 py-0.5 bg-gray-600 text-teal-100 drop-shadow-lg">Hello</button>
        <SpecialBox />
    </div>
</template>

<script setup>
const number = useState('number', () => 0);

const increment = () => {
    number.value++;
}
</script>