<template>
    <div class="home">
        <img alt="Vue logo" src="../assets/logo.png" />
        <HelloWorld msg="Welcome to Your Vue.js App" />
        <SlotParam>
            <p slot="a">aaa</p>
        </SlotParam>
    </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import SlotParam from "@/components/Slot.vue";

export default {
    name: "Home",
    components: {
        HelloWorld,
        SlotParam
    }
};
</script>

<style lang="sass" scoped="scoped">
img max-width 120px
</style>