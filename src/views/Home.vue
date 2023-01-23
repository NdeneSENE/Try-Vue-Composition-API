<template>
  <div class="flex flex-wrap flex-grow">
    <PostCard v-for="post in posts" :key="post.id" :post="post" />
  </div>
</template>
<script setup>
import useRessource from "../composables/useRessource";
import PostCard from "../components/PostCard.vue";

const {items: posts, fetchAll} = useRessource('posts')

fetchAll()
</script>
