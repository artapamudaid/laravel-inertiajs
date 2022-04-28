<script setup>

defineProps(
    {
        name: String,
    }
)
</script>

<template>
    <h1>Hello Inertia, I'm {{ name }}</h1>
    <inertia-link :href="`/user`" class="btn btn-primary">Go To Demo</inertia-link>
</template>
