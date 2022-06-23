<template>
    <div class="task">
        <input class="task__checkbox" type="checkbox" />
        <p class="task__content">
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Autem
            delectus omnis maxime soluta iste quisquam obcaecati totam, ipsam a
            facere, exercitationem deserunt perferendis ab unde, est ducimus
            nesciunt ut! Dolorem.
        </p>
        <div class="task__actions flex">
            <Action />
            <!-- <span class="actions__action flex">
                <Icon
                    icon="icomoon-free:bin"
                    color="black"
                    width="16"
                    height="16"
                />
                Delete
            </span>
            <span class="actions__action flex">
                <Icon
                    icon="akar-icons:edit"
                    color="black"
                    width="16  "
                    height="16"
                />
                Edit
            </span> -->
        </div>
    </div>
</template>

<script setup>
import { Icon } from "@iconify/vue";
import Action from "./Action.vue";
</script>

<style scoped>
.task {
    display: grid;
    grid-template-columns: 3rem 95%;

    grid-template-areas:
        "task__checkbox task__content"
        ". task__actions";
}
.task__checkbox {
    grid-area: task__checkbox;
    margin-top: 0.4em;
    display: inline-block;
    justify-self: center;
}

.task__content {
    grid-area: task__content;
}

.task__actions {
    grid-area: task__actions;
    gap: 2rem;

    margin-top: 2rem;
}
</style>