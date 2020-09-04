<template>
    <div></div>
</template>

<script>
export default {
    name: "Calc",
    props: {
        title: string
    },
    data() {
        return {
            msg: "Enter Expression",
            fomula: 0
        };
    },
    methods: {
        doAction() {
            // テキストを改行コードで分割
            const arr = this.fomula.trim().split("¥n");
            // 配列の最後を取り出す
            const last = arr.pop();
            const fn = "";
            for (let n in arr) {
                if (arr[n].trim() != "") {
                    fn += "var" + arr[n] + ";";
                }
            }
        }
    }
};
</script>

<style lang="scss" scoped="scoped"></style>
