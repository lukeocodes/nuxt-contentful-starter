<template>
  <div>
    <p v-if="$fetchState.pending">Fetching posts...</p>
    <p v-else-if="$fetchState.error">An error occurred :(</p>
    <div v-else>
      <ul
        v-if="posts.items.length > 0"
        class="grid gap-16 lg:grid-cols-3 lg:gap-x-5 lg:gap-y-12"
      >
        <li
          v-for="(post, index) in posts.items"
          :key="index"
          class="flex flex-col"
        >
          <MetaPost :post="post" />
        </li>
      </ul>
      <p v-else>No posts...</p>
    </div>
  </div>
</template>

<script>
import { createClient } from "~/plugins/contentful.js";

const client = createClient();

export default {
  data() {
    return {
      posts: [],
    };
  },

  async fetch() {
    this.posts = await client.getEntries({
      content_type: "blogPost",
      order: "-sys.createdAt",
    });
  },
};
</script>
