<template>
    <!-- <button>{{ text }}</button> OR -->
    <button @click="handleButtonClicked">
        {{ props.text }}
    </button>
</template>

<script setup>
const props = defineProps({
    text: {
        type: String,
        default: "No text specified"
    },
})
const emit = defineEmits(['buttonClicked'])
const handleButtonClicked = () => {
    emit('buttonClicked')
}
// access to this props in script section
console.log(props.text);
</script>

<!--
<script>
export default {
    props: {
        text: {
            type: String,
            default: "No text specified"
        }
    },
    emits: ['buttonClicked']
}
</script>
-->