<template>
    <!-- <button>{{ text }}</button> OR -->
    <button @click="$emit('buttonClicked')">
        {{ props.text }}
    </button>
</template>

<script setup>
const props = defineProps({
    text: {
        type: String,
        default: "No text specified"
    },
    //emits: ['buttonClicked'] // it works also
})
const emits = defineEmits(['buttonClicked'])
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