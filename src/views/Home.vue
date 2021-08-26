<template>
  <div class="home">
    <h2>Search</h2>
    <input type="text" v-model="search" />
    <p>Searched term {{ search }}</p>
    <div v-if="matchingList.length">
      <div v-for="name in matchingList" :key="name">
        {{ name }}
      </div>
    </div>
    <div v-else>
      can't be found that
    </div>
  </div>
</template>

<script>
import { ref, reactive, computed } from "@vue/reactivity";
export default {
  name: "Home",
  setup() {
    const search = ref("");
    const names = ref(["ahmed", "sadiq", "nimco", "asiya"]);

    const matchingList = computed(() => {
      return names.value.filter((name) => name.includes(search.value));
    });
    return { search, names, matchingList };
  },
};
</script>
