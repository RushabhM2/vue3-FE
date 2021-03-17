<template>
  <div>Hello {{name}} {{channel}}</div>
  <div v-html="channel"></div>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Disabled Button</button>
  <h1 v-bind:class="isSoldOut ? 'new' : 'green'">Conditional rendering header</h1>
  <h2 v-bind:class="[isSoldOut ? 'new' : 'green', 'promoted']">Newly promoted movie</h2>
  <h2 v-bind:class="{
    promoted: isPromoted,
    new: !isSoldOut,
    green: isSoldOut
  }">Newly promoted movie object</h2>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: 'Rushabh',
      channel: '<b>Human Motion</b>',
      isDisabled: true,
      isSoldOut: false,
      isPromoted: true
    };
  },
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

.new {
  color: red;
}

.green {
  color: green;
}

.promoted {
  background-color: bisque;
}
</style>
