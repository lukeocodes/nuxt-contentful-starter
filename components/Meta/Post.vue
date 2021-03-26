<template>
  <div>
    <nuxt-link :to="post.fields.slug" class="flex-grow block mt-4">
      <p class="text-xl font-semibold text-gray-900">
        {{ post.fields.title }}
      </p>
      <p class="mt-3 text-base text-gray-500">
        {{ post.fields.description }}
      </p>
    </nuxt-link>
    <MetaAuthor :author="post.fields.author" />
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>
