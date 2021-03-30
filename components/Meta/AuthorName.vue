<template>
  <MetaAuthorLink :author="author">
    {{ author.fields.name }}
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
