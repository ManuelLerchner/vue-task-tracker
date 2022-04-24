<template>
    <div :key="task.id" v-for="task in tasks">
        <Task @delete-task="$emit('delete-task', task.id)" :task="task" />
    </div>
</template>

<script lang="ts">
import Task from "./Task.vue";
export default {
    name: "Tasks",
    props: {
        tasks: {
            type: Array,
            required: true,
        },
    },
    components: { Task },
    emits: ["delete-task"],
};
</script>
