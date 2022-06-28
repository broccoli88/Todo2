<template>
    <div class="task">
        <input class="task__checkbox" type="checkbox" />
        <p class="task__content">{{ task.content }}</p>
        <div class="task__actions flex">
            <Action>
                <template v-slot:delete-task>
                    <div @click="removeTask" class="action__button flex">
                        <Icon
                            icon="icomoon-free:bin"
                            color="black"
                            width="16"
                            height="16"
                        />
                        Delete
                    </div>
                </template>
            </Action>
        </div>
    </div>
</template>

<script setup>
import { Icon } from "@iconify/vue";
import Action from "./Action.vue";

const emits = defineEmits(["remove-task"]);
const props = defineProps(["task"]);

// REMOVING TASK
const removeTask = () => {
    let taskId = props.task.taskId;

    emits("remove-task", taskId);
};
</script>

<style scoped>
.task {
    display: grid;
    grid-template-columns: 3rem 95%;

    grid-template-areas:
        "task__checkbox task__content"
        ". task__actions";

    align-items: stretch;
}
.task__checkbox {
    grid-area: task__checkbox;
    margin-top: 0.4em;
    display: inline-block;
    justify-self: start;
    width: 20px;
    height: 20px;
}

.task__content {
    grid-area: task__content;
}

.task__actions {
    grid-area: task__actions;
    margin-top: 2rem;
}

.action__button {
    margin-right: 2rem;
    align-items: center;
    gap: 0.6rem;
}
</style>