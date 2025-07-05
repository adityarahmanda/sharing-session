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
  >
    <span ref="slotParent" class="opacity-0"><slot></slot></span>
    <span style="--index: 0;">
      <span class="original-text">{{ originalText }}</span>
      <span class="shuffled-text">{{ shuffledTexts[0] }}</span>
    </span>
    <span style="--index: 1;">
      <span class="original-text">{{ originalText }}</span>
      <span class="shuffled-text">{{ shuffledTexts[1] }}</span>
    </span>
    <span style="--index: 2;">
      <span class="original-text">{{ originalText }}</span>
      <span class="shuffled-text">{{ shuffledTexts[2] }}</span>
    </span>
  </annotate>
</template>

<script setup>
import { useNav } from '@slidev/client';
import { ref, onMounted } from 'vue';

const props = defineProps({
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

const { clicks, currentSlideNo } = useNav();
const slotParent = ref(null);
const originalText = ref('');
const shuffledTexts = ref(['', '', '']);

onMounted(() => {
  originalText.value = slotParent.value?.textContent || '';
  for (let i = 0; i < 3; i++) {
    shuffledTexts.value[i] = shuffleString(originalText.value);
  }
});

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