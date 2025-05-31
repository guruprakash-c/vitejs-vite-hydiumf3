<script setup>
import { reactive } from 'vue';
let initial = reactive({ val: { count : 0}, users: ['Mary'] });
const Modifyuser = () => {
    initial.users[0] = "Monica";
};
const Removeuser = () => {
    initial.users.pop();
};
const Adduser = () => {
    initial.users.push("Arnold");
};
</script>

<template>
    <article>
        <h1>Reactive Components</h1>
        <h2>initial value: {{ initial.val.count }}</h2>
        <pre>initial users: {{ initial.users }}</pre>
        <div class="btn-group">
            <button class="btn btn-primary" @click="initial.val.count+=5">[+] Add 5</button>
            <button class="btn btn-info" @click="Adduser">[+] Add New user</button>
            <button class="btn btn-secondary" @click="Modifyuser">[/] Modify New user</button>
            <button class="btn btn-danger" @click="Removeuser">[-] Remove a user</button>
        </div>
    </article>
</template>