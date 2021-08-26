<template>
  <div class="post">
    <h1>
      {{ post.title }}
    </h1>
    <p>{{ snippet }}</p>
  </div>
</template>

<script>
export default {
  props: ["post"],
  setup(props) {
    const snippet = props.post.body.substring(0, 90) + " ...";

    return { snippet };
  },
};
</script>

<style>
.post {
  text-align: left;
  width: 60%;
  margin: auto;
  background: rgb(66, 66, 66);
  padding: 1rem;
  margin-bottom: 1rem;
  border-radius: 0.3rem;
  color: white;
  cursor: pointer;
}
</style>
