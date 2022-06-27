
<template>
    <div class="wrapper flex-column">
        <h1>To Do List</h1>
        <TasksList />
    </div>
</template>


<script setup>
import TasksList from "../components/TasksList.vue";
</script>

<!-- Create less complex situation to not prop and emit everywhere -->
<style scoped>
.wrapper {
    max-width: 100vw;
    min-height: 100vh;

    padding: 4rem 3rem;

    background-color: var(--color-bg);

    align-items: center;
    gap: 4rem;

    overflow-y: hidden;
}
</style>