<template>
  <div v-for="post in posts" :key="post.id"></div>
</template>

<script>
export default {
  props: ["posts"],
};
</script>

<style></style>
