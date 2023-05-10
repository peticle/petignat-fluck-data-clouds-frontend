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
        background: #01a2a6;
        border-radius: 2em;
        color: #f2f2f2;
        display: block;
        font-family: 'Roboto', arial;
        font-size: 1.2em;
        padding: .4em .6em;
        text-align: center;
        transition: background .2s;
        user-select: none;

        &:hover {
            background: #20acb0;
            cursor: pointer;
        }

        &:active {
            background: #049B9F;
        }
    }
}
</style>
