<template>
    <div id="app">
        <div id="nav">
            <router-link to="/">Home</router-link>&nbsp;|&nbsp;
            <router-link to="/about">About</router-link>&nbsp;|&nbsp;
            <router-link to="/props">Props</router-link>&nbsp;|&nbsp;
            <router-link to="/slot">Slot</router-link>
        </div>
        <router-view />
    </div>
</template>

<style lang="stylus">
#app
    font-family Avenir, Helvetica, Arial, sans-serif
    -webkit-font-smoothing antialiased
    -moz-osx-font-smoothing grayscale
    text-align center
    color #2c3e50
    margin-top 60px
</style>
