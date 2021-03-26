<template>
  <div class="flex items-center mt-6">
    <div class="flex-shrink-0">
      <a href="#">
        <span class="sr-only"> {{ author.fields.name }} </span>
        <img class="w-10 h-10 rounded-full" src="pic.png" alt="" />
      </a>
    </div>
    <div class="ml-3">
      <p class="text-sm font-medium text-gray-900">
        <a href="#"> {{ author.fields.name }} </a>
      </p>
      <div class="flex space-x-1 text-sm text-gray-500">
        <time datetime="2020-03-16"> Mar 16, 2020 </time>
        <span aria-hidden="true"> &middot; </span>
        <span> 6 min read </span>
      </div>
    </div>
  </div>
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
