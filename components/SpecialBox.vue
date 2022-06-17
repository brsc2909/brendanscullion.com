<template >
    <div class="chamfer bg-teal-200 w-56 h-auto px-0.5 py-0.5 shadow-2xl drop-shadow-2xl overflow-hidden">
        <div class="chamfer w-auto h-auto px-9 py-1 opacity-25 bg-gray-800 text-teal-100">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Commodi fugiat quos obcaecati distinctio, itaque
            dolorum velit et officiis necessitatibus, optio quam expedita quod earum illo! Illo rerum sapiente
            laudantium veritatis?
        </div>
    </div>
</template>

<style scoped>
.chamfer {
    --chamfer: 15px;
    clip-path: polygon(0 calc(0+var(--chamfer)),
            0 calc(100% - var(--chamfer)),
            calc(0+var(--chamfer)) 100%,
            calc(100% - var(--chamfer)) 100%,
            100% calc(100% - var(--chamfer)),
            100% calc(0+var(--chamfer)),
            calc(100% - var(--chamfer)) 0,
            calc(0+var(--chamfer)) 0);
}
</style>