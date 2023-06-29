<script setup>
defineProps({
  reverse: {
    type: Boolean,
    default: false
  }
})
</script>
<template>
  <transition
    enter-active-class="transition duration-200"
    leave-active-class="transition duration-200"
    :enter-from-class="`opacity-0 ${!reverse ? '-translate-x-2' : 'translate-x-2'} `"
    :leave-to-class="`opacity-0 ${!reverse ? '-translate-x-2' : 'translate-x-2'} `"
  >
    <slot />
  </transition>
</template>
