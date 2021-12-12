<template>
    <Header/>
</template>

<script lang="ts">
    import {Vue,Options} from "vue-class-component"
    import Header from "../components/Header.vue"

    @Options({
        components: {
            Header
        }
    })

    export default class Flow extends Vue {
        a:string="Hello"
    }
</script>

<style lang="scss" scoped>

</style>