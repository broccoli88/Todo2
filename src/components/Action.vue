<template>
    <div class="action flex">
        <slot name="delete-task"> </slot>
    </div>
</template>

<script setup>
</script>

<style scoped>
.action {
    align-items: center;
    gap: 0.5rem;

    color: var(--color-accent);

    cursor: pointer;
}
</style>
