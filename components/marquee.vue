<template>
  <component :is="$attrs.tag || 'div'" ref="root" class="relative w-full overflow-hidden">
    <div class="invisible py-2 whitespace-nowrap" aria-hidden="true">Marquee Text Placeholder</div>
    <div class="absolute left-0 top-1/2 -translate-y-1/2 whitespace-nowrap"
        :class="[direction === 'left' ? 'anim-marquee-left' : 'anim-marquee-right']"
        :style="{ animationDuration: duration + 's !important' }">
      <slot />
    </div>
    <div class="absolute left-0 top-1/2 -translate-y-1/2 whitespace-nowrap"
        :class="[direction === 'left' ? 'anim-marquee-left-2' : 'anim-marquee-right-2']"
        :style="{ animationDuration: duration + 's !important' }">
      <slot />
    </div>
  </component>
</template>

<script setup>
const props = defineProps({
  direction: {
    type: String,
    default: 'left',
    validator: value => ['left', 'right'].includes(value)
  },
  duration: {
    type: Number,
    default: 30
  }
});
</script>

<style scoped>
@keyframes marquee-left {
    0% {
        transform: translate(0%, -50%);
    }
    49.999% {
        transform: translate(-100%, -50%);
        opacity: 1;
    }
    50% {
        transform: translate(100%, -50%);
        opacity: 0;
    }
    50.001% {
        opacity: 1;
    }
    100% {
        transform: translate(0%, -50%);
    }
}

@keyframes marquee-left-2 {
    0% {
        transform: translate(100%, -50%);
    }
    100% {
        transform: translate(-100%, -50%);
    }
}

@keyframes marquee-right {
    0% {
        transform: translate(0%, -50%);
    }
    49.999% {
        transform: translate(100%, -50%);
        opacity: 1;
    }
    50% {
        transform: translate(-100%, -50%);
        opacity: 0;
    }
    50.001% {
        opacity: 1;
    }
    100% {
        transform: translate(0%, -50%);
    }
}

@keyframes marquee-right-2 {
    0% {
        transform: translate(-100%, -50%);
    }
    100% {
        transform: translate(100%, -50%);
    }
}

.anim-marquee-left {
  animation: marquee-left 30s linear infinite;
}

.anim-marquee-left-2 {
  animation: marquee-left-2 30s linear infinite;
}

.anim-marquee-right {
  animation: marquee-right 30s linear infinite;
}

.anim-marquee-right-2 {
  animation: marquee-right-2 30s linear infinite;
}
</style>