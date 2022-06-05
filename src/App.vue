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
<!-- <template>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
</template> -->


<!--------------------- Binding Classes -------------------------->
<template>
  <h2 class="underline">Underlined Text</h2>
  <h2 class="underline" v-bind:class="status">Status</h2>
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 v-bind:class="isSoldOut ? 'sold-out' : 'new'">Soldout moive</h2>
  <h2 v-bind:class="['new', 'promoted']">Newly promoted movie</h2>
  <h2 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']">Array Conditional movie</h2>
  <h2 v-bind:class="{
    promoted: isPromoted,
    new: !isSoldOut,
    'sold-out': isSoldOut,
  }">Object Conditional movie</h2>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      greet: 'Hello',
      name: 'Raihan',
      channel: 'RaihanWebmaster',
      hero: '<b>Raihan</b>',
      hack: `<a href="#" onclick="alert('You have been hacked!')">Win a prize!</a>`,
      headingId: 'heading',
      isDisabled: true,
      status: 'danger',
      isPromoted: true,
      isSoldOut: false,
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

.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: olivedrab
}

.sold-out {
  color: red;
}
</style>
