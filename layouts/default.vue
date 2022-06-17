<template>
    <div>
        <header>
            <slot name="navbar">
                <TopNav />
            </slot>
        </header>
        <main>
            <slot />
        </main>
        <footer class="absolute bottom-0">
            <slot name="footer">
                <TopNav />
            </slot>
        </footer>
    </div>
</template>