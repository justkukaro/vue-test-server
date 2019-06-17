<template>
    <div id="app">
        <input type="button" value="첫번째 사진" @click="on01Click">
        <input type="button" value="두번째 사진" @click="on02Click">
        <first v-if="is_01"></first>
        <second v-else-if="is_02"></second>
    </div>
</template>

<script>
    import first from './components/first'
    import second from './components/second'

    export default {
        name: 'app',
        components: {
            first,
            second
        },
        data(){
            return {
                is_01: false,
                is_02: false,
            }
        },
        methods:{
            on01Click(){
                this.is_01 = true;
                this.is_02 = false;
            },
            on02Click(){
                this.is_01 = false;
                this.is_02 = true;
            }
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
