<template>
    <!-- <button>{{ text }}</button> OR -->
    <button>{{ props.text }}</button>
</template>

<script setup>
const props = defineProps({
    text: {
        type: String,
        default: "No text specified"
    }
})
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
    }
}
</script>
-->