<template>
    <component :is="$attrs.tag || 'div'" ref="root" v-bind="$attrs">
    </component>
</template>

<script setup>
import { onMounted, ref } from 'vue';

const props = defineProps({
  tweetId: {
    type: String,
    required: true
  },
  tweetMaxWidth: {
    type: Number,
    default: 550
  }
});

const root = ref(null);

onMounted(async () => {
  await waitForTwitterReady();
  await window.twttr.ready();

  root.value.innerHTML = '';
  window.twttr.widgets.createTweet(props.tweetId, root.value, {
    width: props.tweetMaxWidth,
    align: 'center',
  });
});

function waitForTwitterReady(maxTries = 20, interval = 300) {
  return new Promise((resolve, reject) => {
    let tries = 0;
    const check = () => {
      if (window.twttr?.ready) {
        window.twttr.ready().then(resolve);
      } else if (tries++ < maxTries) {
        setTimeout(check, interval);
      } else {
        reject(new Error('Twitter widgets.js did not load in time'));
      }
    };
    check();
  });
}

</script>

<style scoped>
.twitter-tweet {
  margin-top: 0;
  margin-bottom: 0;
}

:deep(.twitter-tweet) {
  margin-top: 0 !important;
  margin-bottom: 0 !important;
}
</style>