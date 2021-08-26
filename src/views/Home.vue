<template>
  <h1>Posts</h1>
  <div v-if="showPosts">
    <PostsList :posts="posts" />
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";
import PostsList from "../components/PostsList.vue";
export default {
  components: { PostsList },
  setup() {
    const posts = ref([
      {
        id: 1,
        title: "top 5 css frameworks",
        body:
          "tempor felis ac facilisis. Praesent fermentum elit ut metus dapibus, sed suscipit ante ultricies. Nunc ornare lacus at lacus euismod consequat. In hac habitasse platea dictumst. Integer et dui volutpat, pretium arcu vitae, porttitor libero. Aliquam sed velit placerat, ultrices magna congue, molestie urna. Nunc vehicula augue sed orci euismod sodales. In ac fringilla libero, in dignissim sem. Cras maximus mauris et neque volutpat vulputate.",
      },
      {
        id: 2,
        title: "How to check if my softeware is updated",
        body:
          "tempor felis ac facilisis. Praesent fermentum elit ut metus dapibus, sed suscipit ante ultricies. Nunc ornare lacus at lacus euismod consequat. In hac habitasse platea dictumst. Integer et dui volutpat, pretium arcu vitae, porttitor libero. Aliquam sed velit placerat, ultrices magna congue, molestie urna. Nunc vehicula augue sed orci euismod sodales. In ac fringilla libero, in dignissim sem. Cras maximus mauris et neque volutpat vulputate.",
      },
    ]);

    const showPosts = ref(true);
    return { posts, showPosts };
  },
};
</script>

<style></style>
