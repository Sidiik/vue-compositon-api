<template>
  <div v-for="post in posts" :key="post.id">
    <PostItem :post="post" />
  </div>
</template>

<script>
import PostItem from "./PostItem.vue";
import { onMounted, onUnmounted, onUpdated, ref } from "@vue/runtime-core";
export default {
  props: ["posts"],
  components: { PostItem },
  setup() {},
};
</script>

<style></style>
