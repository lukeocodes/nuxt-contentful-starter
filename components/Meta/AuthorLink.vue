<template>
  <nuxt-link :to="`authors/${author.fields.slug}`">
    <slot></slot>
  </nuxt-link>
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
