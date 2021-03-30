<template>
  <div v-if="author">
    <MetaAuthorName :author="author" />
    <p v-if="author.wasBuild">I WAS BUILT WITH THE GENERATE FUNCTION</p>
  </div>
</template>

<script>
// import VueMarkdown from "@adapttive/vue-markdown";
import { createClient } from "~/plugins/contentful.js";

const client = createClient();

export default {
  components: {
    // VueMarkdown,
  },

  async asyncData({ payload, params: { slug } }) {
    if (payload) {
      return { author: payload };
    } else {
      const authors = await client.getEntries({
        content_type: "person",
        "fields.slug[in]": slug,
        limit: 1,
      });

      return {
        author: authors.items[0],
      };
    }
  },

  data() {
    return {
      author: null,
    };
  },
};
</script>
