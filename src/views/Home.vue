<template>
  <div class="home">
    <h1>Home</h1>
    <p ref="paragraph">my name is {{ name }} and my age is {{ age }}</p>
    <input type="text" v-model="name" />
    <button @click="handleClick">Click me</button>
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";
export default {
  name: "Home",
  setup() {
    const paragraph = ref(null);
    const name = ref("sidiik");
    const age = ref(45);
    const handleClick = () => {
      name.value = "sidiik omar";
      age.value = 34;
    };
    console.log(paragraph);

    return { handleClick, paragraph, name, age };
  },
};
</script>
