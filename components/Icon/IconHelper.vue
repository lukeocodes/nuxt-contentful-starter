<template>
  <span class="svg-icon svg-baseline">
    <slot></slot>
  </span>
</template>

<style scoped>
.svg-icon {
  display: inline-flex;
  align-self: center;
  top: 0.125em;
  position: relative;
}
.svg-icon >>> svg {
  height: 1em;
  width: 1em;
  fill: currentColor;
}
</style>
