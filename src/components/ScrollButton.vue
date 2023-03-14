<template>
    <div
        class="scroll-button"
        :class="isUp ? `up` : `down`"
        @click="handleScroll"
    ></div>
</template>

<script setup>
import { defineProps, computed } from "vue";

const props = defineProps({
    type: {
        type: String,
        default: "down",
    },
});

const isUp = computed(() => props.type === "up");

function handleScroll() {
    if (isUp.value) {
        window.scrollTo({
            left: 0,
            top: 0,
            behavior: "smooth",
        });
    }
}
</script>

<style lang="scss" scoped></style>
