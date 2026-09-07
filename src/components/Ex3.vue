<script setup>
    import { ref } from 'vue'

    const loginType = ref('username')

    const username = ref('')
    const email = ref('')
    
    
</script>

<template>
    <h1>Please select your login option</h1>
    <select v-model="loginType">
        <option value="username">Username login</option>
        <option value="email">Email login</option>
    </select>

    <br><br>
    <div v-if="loginType === 'username'">
        <label>Username</label>
        <input type="text" placeholder="Enter your username" v-model="username">
    </div>

    <div v-else>
        <label>Email</label>
        <input type="email" placeholder="Enter your email" v-model="email">
    </div>
    
</template>

