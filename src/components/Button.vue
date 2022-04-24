<template>
    <button @click="onClick()" :style="{ background: color }" class="btn">{{ text }}</button>
</template>

<script lang="ts">
export default {
    name: "Button",
    props: {
        text: {
            type: String,
            required: true,
        },
        color: {
            type: String,
            required: false,
            default: "black",
        },
    },
    methods: {
        onClick() {
         console.log("Button clicked!");
        },
    },
};
</script>
