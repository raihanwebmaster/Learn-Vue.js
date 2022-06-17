<!---------------------- v-once v-pre ------------------------->
<!-- v-once -> 
    Renders the corresponding HTML  element only once . On subsequent re-renders, the element is treated as static content and skipped. -->
<!-- v-pre -> 
  Skips compilation for the corresponding element -->
<template>
    <h2 v-once>{{name}}</h2>
    <button @click="name = 'uddin'">Change Name</button>
    <h2 v-pre>{{name}}</h2>
</template>



<script>
export default {
  name: "App",
  data() {
    return {
      name: 'raihan'
    };
  },
  methods: {
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}


</style>
