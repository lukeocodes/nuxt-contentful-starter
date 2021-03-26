<template>
  <article v-if="post" class="prose prose-lg xl:prose-xl max-w-none">
    <MetaAuthor :author="post.fields.author" />
    <h1>{{ post.fields.title }}</h1>
    <blockquote class="p-8 text-lg bg-blue-100 border-l-4 border-blue-600">
      {{ post.fields.description }}
    </blockquote>
    <p v-if="post.wasBuild">I WAS BUILT WITH THE GENERATE FUNCTION</p>
    <vue-markdown>{{ post.fields.body }}</vue-markdown>
  </article>
</template>

<script>
import VueMarkdown from "@adapttive/vue-markdown";
import { createClient } from "~/plugins/contentful.js";

const client = createClient();

export default {
  components: {
    VueMarkdown,
  },

  async asyncData({ payload, params: { slug } }) {
    if (payload) {
      return { post: payload };
    } else {
      const posts = await client.getEntries({
        content_type: "blogPost",
        "fields.slug[in]": slug,
        limit: 1,
      });

      return {
        post: posts.items[0],
      };
    }
  },

  data() {
    return {
      post: null,
    };
  },
};
</script>
