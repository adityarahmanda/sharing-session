<template>
  <div class="glitch" style="--stacks: 3;" v-bind="$attrs">
    <span style="--index: 0;" :data-original="text" :data-translated="shuffleString(text)"></span>
    <span style="--index: 1;" :data-original="text" :data-translated="shuffleString(text)"></span>
    <span style="--index: 2;" :data-original="text" :data-translated="shuffleString(text)"></span>
  </div>
</template>

<script setup>
const props = defineProps({
  text: String,
  translated: String
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