<template>
    <div>
        <h2>Props</h2>
        <div class="lay">
            <div class="org">
                <div class="mol">
                    <article-post></article-post>
                </div>
                <div class="mol">
                    <article-post article-num="66" article-title="人間錯覚"></article-post>
                </div>
                <div class="mol">
                    <ul v-for="(item, index) in books" :key="index">
                        <li>{{ item.articleNum}} {{ item.articleTitle}}</li>
                    </ul>
                    <!-- <article-post article-num="2" article-title="人間錯覚"></article-post> -->
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import ArticlePost from "@/components/ArticlePost.vue";

export default {
    data() {
        return {
            hel: "hel",
            books: [
                {
                    articleNum: 1,
                    articleTitle: "人間合格"
                },
                {
                    articleNum: 2,
                    articleTitle: "人間錯覚"
                },
                {
                    articleNum: 3,
                    articleTitle: "人間錯誤"
                }
            ]
        };
    },
    components: {
        ArticlePost
    }
};
</script>

<style lang="stylus" scoped="scoped"></style>
