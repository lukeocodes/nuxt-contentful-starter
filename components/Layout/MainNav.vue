<template>
  <nav>
    <StructureMaxWidth class="h-16 md:flex md:items-center md:justify-between">
      <div class="flex space-x-6 md:space-x-0">
        <div class="md:hidden">
          <button class="overflow-hidden text-black" @click="open = !open">
            <IconDotsHorizontal :open="open" />
          </button>
        </div>
        Logo
      </div>
      <div>
        <ul
          class="md:flex md:space-x-6 md:block"
          :class="{ block: open, hidden: !open }"
        >
          <li><nuxt-link to="/">Home</nuxt-link></li>
        </ul>
      </div>
    </StructureMaxWidth>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      open: false,
    };
  },
};
</script>
