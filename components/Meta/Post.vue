<template>
  <div>
    <nuxt-link :to="`/${post.fields.slug}`" class="flex-grow block mt-4">
      <p class="text-xl font-semibold text-gray-900">
        {{ post.fields.title }}
      </p>
      <p class="mt-3 text-base text-gray-500">
        {{ post.fields.description }}
      </p>
    </nuxt-link>
    <div class="flex items-center mt-6">
      <div class="flex-shrink-0">
        <MetaAuthorImage :author="post.fields.author" />
      </div>
      <div class="ml-3">
        <p class="text-sm font-medium text-gray-900">
          <MetaAuthorName :author="post.fields.author" />
        </p>
        <div class="flex space-x-1 text-sm text-gray-500">
          <time datetime="2020-03-16"> Mar 16, 2020 </time>
          <span aria-hidden="true"> &middot; </span>
          <span> 6 min read </span>
        </div>
      </div>
    </div>
    <!-- <MetaAuthorName :author="post.fields.author" /> -->
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
