<script setup lang="ts">
import { ref } from 'vue';

// Props
const props = defineProps({
    label: {
        type: String,
        required: true,
    },
    min: {
        type: Number,
        required: true,
    },
    max: {
        type: Number,
        required: true,
    },
});

// Datas
const id: string = props.label.toLowerCase().substring(0, 5);

// Value
const value = ref(props.min);
</script>

<template>
    <div class="slider">
        <input v-model="value" type="range" :min="min" :max="max">
        <input :id="`in-${id}`" type="number" :value="value">
        <label :for="`in-${id}`">{{ label }}</label>
    </div>
</template>

<style lang="scss">
div.slider {
    color: #554348;
    display: flex;
    flex-direction: row-reverse;
    flex-wrap: wrap-reverse;
    font-family: 'Roboto', arial;
    gap: .4rem .6rem;
    padding: .6em;

    >input:last-of-type {
        text-align: center;
        appearance: textfield;
        -moz-appearance: textfield;
        border: none;
        outline: none;
        width: 2em;

        &::-webkit-outer-spin-button,
        &::-webkit-inner-spin-button {
            -webkit-appearance: none;
            margin: 0;
        }

        &:valid~label {
            color: #01a2a6;
        }
    }

    >input:first-of-type {
        flex-grow: 1;

        &:hover {
            cursor: pointer;
        }
    }

    >label {
        flex: 0 1 100%;
    }
}
</style>
