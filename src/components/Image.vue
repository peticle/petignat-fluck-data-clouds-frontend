<script setup lang="ts">
// Props
const props = defineProps({
    src: {
        type: String,
        required: true,
    },
    size: {
        type: String,
        required: true,
    },
    alt: String,
});
</script>

<template>
    <div class="image">
        <img :src="src" :alt="alt">
    </div>
</template>

<style lang="scss">
div.image {
    overflow: hidden;
    text-align: center;

    >img {
        background: #d7d7d8;
        border-radius: 4px;
        height: v-bind(size);
        object-fit: cover;
        padding: 1px;
        width: v-bind(size);
    }
}
</style>
