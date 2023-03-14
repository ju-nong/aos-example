<template>
    <Main />
    <Sample
        v-for="({ name, options }, index) in aosConfig"
        :key="index"
        :name="name"
        :options="options"
    />
</template>

<script setup>
import { onMounted, getCurrentInstance } from "vue";
import { Main, Sample } from "@components";

const aosConfig = [
    {
        name: "fade",
        options: [
            "up",
            "down",
            "right",
            "left",
            "up-right",
            "up-left",
            "down-right",
            "down-left",
        ],
    },
    {
        name: "flip",
        options: ["left", "right", "up", "down"],
    },
    {
        name: "zoom",
        options: [
            "in",
            "in-up",
            "in-down",
            "in-left",
            "in-right",
            "out",
            "out-up",
            "out-down",
            "out-right",
            "out-left",
        ],
    },
];
</script>

<style lang="scss"></style>
