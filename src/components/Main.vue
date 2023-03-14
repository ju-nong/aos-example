<template>
    <div class="w-[100vw] h-[100vh] main-container">
        <div class="title" data-aos="zoom-in">
            <div class="text-4xl font-bold pb-2">스크롤 내려봐요</div>
            <div class="text-xl">슈루루루룩</div>
        </div>
        <div class="icon">
            <ScrollButton />
        </div>
    </div>
</template>

<script setup>
import ScrollButton from "./ScrollButton.vue";
import Aos from "aos";

Aos.init();
</script>

<style lang="postcss"></style>
