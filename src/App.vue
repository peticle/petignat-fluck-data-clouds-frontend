<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <header>
        <h1>Stable Diffusion</h1>
        <nav>
            <RouterLink to="/">Home</RouterLink>
        </nav>
    </header>

    <main>
        <RouterView />
    </main>

    <footer>
        Flück Thierry and Petignat Clément<br>
        &copy; Haute École Arc 2023
    </footer>
</template>

<style scoped lang="scss"></style>
