<script setup>

import {Link} from "@inertiajs/inertia-vue3"
import { Inertia } from "@inertiajs/inertia"


defineProps({
    users: Object,
})

function deleteUser (id) {
    Inertia.delete(`/user/${id}`)
}
</script>

<template>
    
<div class="max-w-7xl mx-20 mt-10">
    <Link :href="`/user/create`" class="btn btn-success">+ Add User</Link>
    <div class="overflow-x-auto mt-5">
        <table class="table w-full">
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
                    <Link :href="`/user/${user.id}/edit`" class="btn btn-warning">Edit</Link>
                    <button @click.prevent="deleteUser(`${user.id}`)" method="delete" class="btn btn-error">Delete</button>
                </td>
            </tr>
        </tbody>
        </table>
    </div>
</div>

</template>