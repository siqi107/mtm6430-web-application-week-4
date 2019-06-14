// create a component in vue cli
// 1. create simba.vue
// 2. import simba.vue to app.vue
// 3. add to the list of component
// 4. use simba tag name in parent template

// use props
// props: property coming from parent
// 1. sending the vaule: use an attribute "treat" on app.vue
// 2. receiving: props["treat"] in simba.vue
// 3. display: {{ treat }} in simba.vue

<template>
  <div>
    <h2>Hello {{ name }}!</h2>
    <ul>
      <li>Age: {{ age }}</li>
      <li>Color: {{ color }}</li>
      <li>{{ treat }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["treat"],
  data: function() {
    return {
      name: "Simba",
      age: 6,
      color: "black"
    };
  }
};
</script>

<style>
h2 {
  color: coral;
}
</style>