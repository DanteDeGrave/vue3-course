<template>
  <div v-if="posts.length">
    <h3>Список постов</h3>
    <ul class="post-list">
      <post-item
        v-for="post in posts"
        :post="post"
        :key="post.id"
        @remove="$emit('remove', post)"
      />
    </ul>
  </div>
  <h2 v-else class="empty">Список постов пуст</h2>
</template>

<script>
import PostItem from "@/components/PostItem.vue";

export default {
  components: {PostItem},
  props: {
    posts: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style scoped>
  .post-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  .empty {
    color: red;
  }
</style>