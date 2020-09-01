<template>
    <div class="div">
        <p>{{ articleNum }}: {{ articleTitle }}</p>
    </div>
</template>

<script>
export default {
    props: {
        articleNum: {
            type: Number,
            default: 1
        },
        articleTitle: {
            type: String,
            default: "未公開"
        }
    }
};
</script>

<style lang="scss" scoped>
</style>