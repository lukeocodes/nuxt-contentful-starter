<template>
  <footer class="pb-40">
    <StructureMaxWidth
      class="py-4 md:py-0 md:h-16 md:flex md:items-center md:justify-between"
    >
      <div class="flex justify-center space-x-6 text-2xl md:order-3">
        <a href="https://twitch.tv/lukeocodes" target="_blank">
          <IconBrandTwitch />
        </a>

        <a href="https://github.com/lukeocodes" target="_blank">
          <IconBrandGitHub />
        </a>

        <a href="https://twitter.com/lukeocodes" target="_blank">
          <IconBrandTwitter />
        </a>

        <a href="https://dev.to/lukeocodes" target="_blank">
          <IconBrandDev />
        </a>

        <a href="https://codepen.io/lukeocodes" target="_blank">
          <IconBrandCodepen />
        </a>
      </div>
      <div class="mt-8 md:mt-0 md:order-2">
        <p class="text-base text-center">
          Sponsored by
          <a href="https://netlify.com" target="_blank">
            <IconBrandNetlify /> Netlify
          </a>
        </p>
      </div>
      <div class="mt-8 md:mt-0 md:order-1">
        <p class="text-base text-center">
          &copy; 2020 whoever it belongs to, probably me but don't @ me.
        </p>
      </div>
    </StructureMaxWidth>
  </footer>
</template>

<script>
export default {};
</script>
