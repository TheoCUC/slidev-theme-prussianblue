<template>
    <div :class="`overflow-auto max-h-${h}`">
        <slot />
    </div>
</template>

<script>
export default {
    props: {
        h: {
            type: String,
            required: false,
            default: 10
        },
    }
}
</script>
