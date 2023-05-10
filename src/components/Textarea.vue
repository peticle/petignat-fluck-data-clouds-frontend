<script setup lang="ts">
// Props
const props = defineProps({
    label: {
        type: String,
        required: true,
    },
    placeholder: String,
    required: Boolean,
});

// Datas
const id: string = props.label.toLowerCase().substring(0, 5);
</script>

<template>
    <div class="textarea">
        <textarea :name="id" :id="`in-${id}`" :placeholder="placeholder" rows="1" :required="required"></textarea>
        <label :for="`in-${id}`">Prompt</label>
    </div>
</template>

<style scoped lang="scss">
div.textarea {
    background: #fff;
    border: solid 1px #cbc7c8;
    border-radius: 5px;
    color: #554348;
    display: flex;
    flex-direction: column-reverse;
    font-family: 'Roboto', arial;
    gap: .4rem 0;
    margin: 1px;
    padding: .4em;

    &:focus-within {
        border: solid 2px #01a2a6;
        margin: 0;
    }

    >textarea {
        border: none;
        font-family: inherit;
        max-height: 8em;
        max-width: 100%;
        min-height: 1.8em;
        min-width: 100%;
        outline: none;
        resize: vertical;

        &:valid~label {
            color: #01a2a6;
        }
    }
}
</style>
