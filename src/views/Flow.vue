<template>
    <Header/>
    <div class="flow d-flex justify-center">
        <div class="container d-flex justify-space">
            <div class="flow__item">
                <FlowItem v-for="x in 4" :key="x"/>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
    import {Vue,Options} from "vue-class-component"
    import Header from "../components/Header.vue"
    import FlowItem from "../components/FlowItem.vue"

    @Options({
        components: {
            Header,
            FlowItem
        }
    })

    export default class Flow extends Vue {
        a:string="Hello"
    }
</script>

<style lang="scss" scoped>

</style>