<template>
  <h1>Step Function Approvals</h1>
  <ApprovalsContainer />
</template>

<script>
import ApprovalsContainer from './components/ApprovalsContainer.vue'

export default {
  name: 'App',
  components: {
    ApprovalsContainer
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
