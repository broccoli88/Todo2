<template>
    <div class="new-task flex-column">
        <h2>Add Task</h2>
        <div class="new-task__add flex-column">
            <textarea v-model="input" id="new-task__content" cols="30" rows="5">
            </textarea>
            <button
                @click="addTask"
                type="submit"
                class="new-task__btn btn-style"
            >
                Add Task
            </button>
        </div>
    </div>
</template>

<script setup>
import { ref } from "@vue/reactivity";

const emits = defineEmits(["new-task"]);

const input = ref("");
const addTask = () => {
    if (input.value === "") return;

    let task = {
        content: input.value,
        taskId: Math.random(),
    };

    emits("new-task", task);
};
</script>

<style scoped>
.new-task {
    width: var(--width);

    padding: var(--main-padding);
    background-color: var(--color-bg2);
    box-shadow: var(--box-shadow-main);
    border-radius: var(--border-radius-big);
}

.new-task__add {
    margin-top: 3rem;
    gap: 1rem;
}

#new-task__content {
    background-color: var(--color-bg);
    border-radius: var(--border-radius-small);

    padding: 2rem 1.2rem;
    font-size: 1.6rem;
}

.new-task__btn {
    width: 100%;
    padding: 0.4em 1em;
    font-size: 1.4rem;
    font-weight: 600;

    text-transform: uppercase;
    box-shadow: var(--box-shadow-subsid);

    border: 0;
    border-radius: var(--border-radius-small);

    cursor: pointer;
}

.new-task__btn:active {
    transform: scale(0.98);
    filter: brightness(92%);
}

.btn-style {
    color: var(--color-font);
    background-color: var(--color-accent);
}
</style>