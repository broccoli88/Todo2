<template>
    <main class="flex-column flex-center">
        <h2>List</h2>
        <Task />
        <Task />
    </main>
</template>

<script setup>
import Task from "./Task.vue";
</script>

<style scoped>
main {
    width: clamp(50%, 80rem, 60%);

    padding: 3rem;
    background-color: var(--color-bg2);

    gap: 3rem;

    border-radius: 15px;
    box-shadow: 0 0 15px 2px hsl(0, 0%, 50%, 0.3);
}
</style>