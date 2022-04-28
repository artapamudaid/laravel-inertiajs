<script setup>
defineProps({
    users: Object,
})
</script>

<template>
    
<div class="max-w-6xl m-auto mt-10">
    <div class="overflow-x-auto">
        <table class="table w-full">
        <!-- head -->
        <thead>
            <tr>
            <th></th>
            <th>Name</th>
            <th>Email</th>
            <th>Action</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(user, index) in users" v-bind:key="user.id">
                <th>{{ index + 1 }}</th>
                <th>{{ user.name }}</th>
                <th>{{ user.email }}</th>
                <td>
                    <a href="" class="btn btn-warning">Edit</a>
                    <a href="" class="btn btn-error">Delete</a>
                </td>
            </tr>
        </tbody>
        </table>
    </div>
</div>

</template>