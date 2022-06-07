<!---------------------- Event Handling ------------------------->
<template>
  <h2>{{ name }}</h2>
  <div>
    <button v-on:click="changeName">Change Name</button>
  </div>
  <!-- <div>
    <button v-on:mouseover="name = 'Uddin'">Change Name</button>
  </div> -->
  <h2>{{ count }}</h2>
  <div>
    <button @click="increment(1, $event)">Increment</button>
    <button v-on:click="decrement(5)">Decrement</button>
  </div>
</template>



<script>
export default {
  name: "App",
  data() {
    return {
      name: 'Raihan',
      count: 0,
    };
  },
  methods: {
    changeName(event) {
      this.name = 'Uddin'
      console.log(event)
    },
    increment(num,event) {
      this.count += num
      console.log('Event',event)
    },
    decrement(num) {
      this.count -= num
    }
  }
};
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
