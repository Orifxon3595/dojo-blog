<template>
  <div class="home">
    Home
    <div v-if="error">{{ error }}</div>
    <div v-if="posts.length">
      <PostsList :posts="posts" />
    </div>
    <div v-else>Loading...</div>
  </div>
</template>

<script>
import PostsList from "../components/PostList.vue";
import getPosts from "../composables/getPsots";

export default {
  name: "HomeView",
  components: { PostsList },
  setup() {
    const { posts, error, load } = getPosts();

    load();

    return {posts, error}
  },
};
</script>
