<template>
  <MetaAuthorLink :author="author">
    <span class="sr-only"> {{ author.fields.name }} </span>
    <img
      class="w-10 h-10 rounded-full"
      :src="author.fields.image.fields.file.url"
      :alt="author.fields.image.fields.title"
    />
  </MetaAuthorLink>
</template>

<script>
export default {
  props: {
    author: {
      type: Object,
      required: true,
    },
  },
};
</script>
