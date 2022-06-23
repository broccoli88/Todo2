<template>
    <div class="action flex">
        <Icon icon="icomoon-free:bin" color="black" width="16" height="16" />
        Delete
    </div>
</template>

<script setup>
import { Icon } from "@iconify/vue";
</script>

<style scoped>
.action {
    align-items: center;
    gap: 0.5rem;

    color: var(--color-accent);

    cursor: pointer;
}
</style>