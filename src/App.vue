<!---------------------- Binding Text ------------------------->
<!-- <template>
  <div>{{greet}} {{name}}</div>
  <div v-text="channel"></div>
</template> -->



<!--------------------- Binding HTML -------------------------->
<!-- <template>
  <div v-html="hero"></div>
  <div v-html="hack"></div>
</template> -->


<!--------------------- Binding to Attributes -------------------------->
<template>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      greet:'Hello',
      name: 'Raihan',
      channel: 'RaihanWebmaster',
      hero: '<b>Raihan</b>',
      hack: `<a href="#" onclick="alert('You have been hacked!')">Win a prize!</a>`,
      headingId: 'heading',
      isDisabled: true,
    }
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
