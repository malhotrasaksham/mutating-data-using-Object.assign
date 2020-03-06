<template>
  <div id="app">
    {{
    a}}
    <button @click="AddProperties">Add Properties</button>
    <button @click="ChangeB">Change b</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      a: {
        a: 1
      }
    };
  },
  methods: {
    ChangeB() {
      if (this.a.hasOwnProperty("b")) this.a.b = 3;
      else alert("First mutate the object");
    },
    AddProperties() {
      this.a = Object.assign({}, this.a, { b: 2 });
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}
</style>
