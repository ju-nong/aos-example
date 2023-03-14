<template>
    <div class="animatnion-container px-[20vw] py-12">
        <p class="title uppercase text-center text-white text-2xl py-4">
            {{ name }}
        </p>
        <div
            v-for="(option, index) in options"
            :key="index"
            class="content"
            :data-aos="`${name}-${option}`"
        >
            <div class="box">
                {{ option }}
            </div>
        </div>
    </div>
</template>

<script setup>
import { defineProps } from "vue";
import Aos from "aos";

Aos.init();

const props = defineProps({
    name: String,
    options: Array,
});
</script>

<style lang="scss" scoped></style>
