<template>
  <annotate 
    ref="root" 
    class="glitch" 
    :class="[
      currentSlideNo == slide && clicks >= showAt && 'show',
      currentSlideNo == slide && clicks >= sortAt && 'sort'
    ]" 
    style="--stacks: 3;" 
    :mark="mark"
    :markAt="markAt"
    :hideMarkAt="hideMarkAt"
    :slide="slide"
    v-bind="$attrs"
  >
    <span style="--index: 0;" :data-original="text" :data-shuffled="shuffledTexts[0]"></span>
    <span style="--index: 1;" :data-original="text" :data-shuffled="shuffledTexts[1]"></span>
    <span style="--index: 2;" :data-original="text" :data-shuffled="shuffledTexts[2]"></span>
  </annotate>
</template>

<script setup>
import { useNav } from '@slidev/client';

const { clicks, currentSlideNo } = useNav();

const props = defineProps({
  text: String,
  showAt: {
    type: Number,
    default: 0
  },
  sortAt: {
    type: Number,
    default: 0
  },
  mark: {
    type: Object,
    default: null
  },
  markDelay: {
    type: Number,
    default: 100
  },
  markAt: {
    type: Number,
    default: 0
  },
  hideMarkAt: {
    type: Number,
    default: -1
  },
  slide: {
    type: Number,
    default: 0
  }
});

const shuffledTexts = Array.from({ length: 3 }, () => shuffleString(props.text));

function shuffleString(str) {
  const splitted = str.split(' ');
  const shuffled = splitted.map(word => {
    return [...word]
      .sort(() => Math.random() - 0.5)
      .join('');
  });
  return shuffled.join(' ');
}
</script>