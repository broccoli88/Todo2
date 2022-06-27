<template>
    <div class="tasks-list flex-column">
        <h2>Tasks List</h2>
        <Task
            @remove-task="deleteTask"
            v-for="task in tasksList"
            :key="task.taskId"
            :task="task"
        />
    </div>
    <NewTask @new-task="addTask" />
</template>

<script setup>
import Task from "./Task.vue";
import NewTask from "./NewTask.vue";
import { reactive } from "@vue/reactivity";

const tasksList = reactive([]);

const addTask = (task) => {
    tasksList.unshift(task);
};

// DELETE TASK -
</script>

<!-- Add DELETE and EDIT actions -->

<style scoped>
.tasks-list {
    width: var(--width);

    padding: var(--main-padding);
    background-color: var(--color-bg2);

    gap: 3rem;

    border-radius: var(--border-radius-big);
    box-shadow: var(--box-shadow-main);
}
</style>