<template>
    <button>{{ text }}</button>
</template>

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