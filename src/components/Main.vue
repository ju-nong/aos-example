<template>
    <div class="w-[100vw] h-[100vh] main-container">
        <div class="title" data-aos="zoom-in">
            <div class="text-4xl font-bold pb-2">스크롤 내려봐요</div>
            <div class="text-xl">슈루루루룩</div>
        </div>
        <div class="icon">
            <div @click="downScrolling"></div>
        </div>
    </div>
</template>

<script setup>
import { defineProps } from "vue";
import Aos from "aos";

Aos.init();

const props = defineProps({
    into: {
        type: Number,
        default: null,
    },
});

function downScrolling() {
    if (!props?.into) {
        return;
    }
    const $into = document.getElementById(`into${props.into}`);

    $into.scrollIntoView({ behavior: "smooth" });

    // 100vh만큼 내려가는 거
    // window.scrollTo({
    //     left: 0,
    //     top: window.pageYOffset + window.innerHeight,
    //     behavior: "smooth",
    // });
}
</script>

<style lang="postcss"></style>
