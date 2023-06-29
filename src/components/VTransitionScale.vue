<template>
  <transition
    enter-active-class="transition duration-200"
    leave-active-class="transition duration-200"
    enter-from-class="opacity-0 scale-0"
    leave-to-class="opacity-0 scale-0"
  >
    <slot />
  </transition>
</template>
