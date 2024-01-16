<script setup>
import task1 from './components/task1.vue'
import { ref, reactive } from 'vue'

const counts = reactive([{ name: 'Task 1', time: 60} , { name: 'Task 2', time: 75},{ name: 'Task 3', time: 95} ]);
function removeTask(){
    counts.splice(0,1);
}
function addTask(){
    counts.push({name: 'Task 4', time: 100});
    alert('task added');
}
</script>
<template>
<div class="container">
    <h1>from task 1</h1>
    <div class="card" v-for="(count , index) in counts" :key="index">
        <div class="card-body"  >
            <p>time: {{count.name}}</p>
            <p>name: {{count.time}}</p>
            <button type="button btn-danger" @click="removeTask()">Remove task</button>
        </div>
        <div>
            <button type="button btn-primary" @click="addTask()">Add task  </button>
        </div>
    </div>
</div>
</template>

<style scoped>

</style>
