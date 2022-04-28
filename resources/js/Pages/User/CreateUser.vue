<script setup>

import { useForm} from "@inertiajs/inertia-vue3"

const form = useForm({
    name: '',
    email: '',
    password: ''
})


</script>

<template>
    <div class="max-w-7xl mx-20 mt-10">
        <form @submit.prevent="form.post('/user')">
            <div class="form-control w-full max-w-xs">
                <label class="label">
                    <span class="label-text">Name</span>
                </label>
                <input type="text" v-model="form.name" placeholder="Type your name here" class="input input-bordered w-full max-w-xs">
            </div>
            <div class="form-control w-full max-w-xs">
                <label class="label">
                    <span class="label-text">Email</span>
                </label>
                <input type="email" v-model="form.email" placeholder="Type your email here" class="input input-bordered w-full max-w-xs">
            </div>
            <div class="form-control w-full max-w-xs">
                <label class="label">
                    <span class="label-text">Password</span>
                </label>
                <input type="password" v-model="form.password" placeholder="Type your password here" class="input input-bordered w-full max-w-xs">
            </div>
            <div class="mt-10">
                <input type="submit" value="Save" class="btn btn-success">
            </div>
        </form>
    </div>
    
</template>
