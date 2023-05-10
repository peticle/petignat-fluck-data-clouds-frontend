<script setup lang="ts">
// Props
const props = defineProps({
    label: {
        type: String,
        required: true,
    },
    required: Boolean,
});

// Emits
const emits = defineEmits(['click']);

// Datas
const id: string = props.label.toLowerCase().substring(0, 5);
</script>

<template>
    <div class="button">
        <input type="button" :name="id" :id="`in-${id}`" :required="required" />
        <label @click="$emit('click')" :for="`in-${id}`">{{ label }}</label>
    </div>
</template>

<style scoped lang="scss">
div.button {

    >input {
        display: none;
    }

    >label {
        background: rgb(1, 162, 166);
        background: linear-gradient(45deg, rgba(1, 162, 166, 1) 0%, rgba(41, 217, 194, 1) 100%);
        border-radius: 2em;
        color: #f2f2f2;
        display: block;
        font-family: 'Roboto', arial;
        font-size: 1.2em;
        padding: .4em .6em;
        text-align: center;
        transition: filter .2s;
        user-select: none;

        &:hover {
            filter: saturate(50%);
            cursor: pointer;
        }

        &:active {
            filter: saturate(150%);
        }
    }
}
</style>
