<template>
  <Flow/>
</template>

<script lang="ts">
import Flow from './views/Flow.vue'
import { Options, Vue } from 'vue-class-component';


@Options({
  components: {
    Flow
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import "./styles/app.scss";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
