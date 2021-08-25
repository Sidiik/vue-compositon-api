<template>
  <div class="home">
    <h1>Home</h1>
    <p>my name is {{ name }} and my age is {{ age }}</p>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  setup() {
    let name = "sadiq";
    let age = "19";

    return { name, age };
  },
};
</script>
