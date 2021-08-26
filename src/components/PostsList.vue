<template>
  <div v-for="post in posts" :key="post.id">
    <PostItem :post="post" />
  </div>
</template>

<script>
import PostItem from "./PostItem.vue";
export default {
  props: ["posts"],
  components: { PostItem },
};
</script>

<style></style>
