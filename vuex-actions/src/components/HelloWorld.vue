<!--HelloWorld.vue-->
<template>
    <div class="hello">
        <b>count : {{this.$store.state.count}}</b><br>
        <b>count^2 : {{this.$store.getters.count}}</b><br>
        <b>random : {{this.$store.getters.random}}</b><br>
        <input type="button" @click="increment()" value="increment"/>
        <input type="button" @click="decrement()" value="decrement"/>
        <input type="button" @click="randomNumber()" value="random"/>
    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
        data() {
            return {}
        },
        created: function () {
        },
        methods: {
            increment: function () {
                this.$store.commit('increment')
            },
            decrement: function () {
                this.$store.commit('decrement')
            },
            randomNumber: function () {
                this.$store.dispatch('generateRandomNumber', /*100*/);
            }
        }
    }
</script>

<style scoped>
</style>
