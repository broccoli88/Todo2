
<template>
    <div class="wrapper flex-column">
        <h1>To Do List</h1>
        <TasksList />
    </div>
</template>


<script setup>
import TasksList from "../components/TasksList.vue";
</script>


<style scoped>
.wrapper {
    width: 100vw;
    height: 100vh;

    padding: 4rem 3rem;

    background-color: var(--color-bg);

    align-items: center;
    gap: 8rem;
}
</style>