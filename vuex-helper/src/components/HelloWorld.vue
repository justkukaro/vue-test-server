<!--HelloWorld.vue-->
<template>
    <div class="hello">
        <b>count : {{cnt}}</b><br>
        <b>count^2 : {{count}}</b><br>
        <b>random : {{$store.getters.random}}</b><br>
        <input type="button" @click="increment()" value="increment"/>
        <input type="button" @click="decrement()" value="decrement"/>
        <input type="button" @click="randomNumber()" value="random"/>
    </div>
</template>

<script>
    import {mapState, mapGetters, mapMutations, mapActions} from 'vuex'

    export default {
        name: 'HelloWorld',
        data() {
            return {}
        },
        created: function () {

        },
        methods: {
            ...mapMutations({
                increment: 'increment',
                decrement: 'decrement'
            }),
            ...mapActions({
                randomNumber: 'generateRandomNumber'
            }),
        },
        computed: {
            ...mapState({
                cnt: 'count',
            }),
            ...mapGetters({
                count: 'count'
            }),
        }
    }
</script>

<style scoped>
</style>
