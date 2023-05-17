<template>
  <div class="backdrop">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <slot>
      </slot>
    </div>
  </div>
</template>

<script>
export default {
  props: ['theme'],
}
</script>
