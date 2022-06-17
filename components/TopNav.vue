<template>
    <nav>
        <div class="py-3 text-center bg-gray-800">
            <NuxtLink v-for="route in $router.options.routes" :key="route.name" :to="route.path"
                class="border px-3 py-2 mx-2 rounded-lg text-teal-100 hover:bg-teal-100 hover:text-gray-800 hover:border-black"
                activeClass="border-black text-gray-800 bg-teal-100">
                {{ route.meta?.name ? route.meta?.name : route.name }}
            </NuxtLink>
        </div>
    </nav>
</template>