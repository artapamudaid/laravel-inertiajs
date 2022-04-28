<script setup>
import {Link} from "@inertiajs/inertia-vue3"

defineProps(
    {
        name: String,
    }
)
</script>

<template>
    <h1>Hello Inertia, I'm {{ name }}</h1>
    <Link :href="`/user`" class="btn btn-primary">Go To Demo</Link>
</template>
