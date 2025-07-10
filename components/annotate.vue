<template>
  <component :is="$attrs.tag || 'div'" ref="root" v-bind="$attrs">
    <slot />
  </component>
</template>

<script setup>
import { ref, onMounted, watch } from 'vue'
import { annotate } from 'rough-notation'
import { useNav } from '@slidev/client'

const { clicks, currentSlideNo, slides } = useNav()

const props = defineProps({
  id: {
    type: String,
    default: ""
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
  }
});

const root = ref(null);
let annotation = null;

onMounted(tryAnnotate);
watch([clicks, currentSlideNo], tryAnnotate);

function tryAnnotate() 
{
  if (props.id != slides.value[currentSlideNo.value - 1].meta.slide.frontmatter.annotateId) 
  {
    if (annotation)
      annotation.hide();
    return;
  }

  if (props.mark && root.value && clicks.value >= props.markAt) {
    if (annotation && annotation.isShowing()) return;

    if (annotation)
      annotation.hide();
    else
      annotation = annotate(root.value, props.mark);
    setTimeout(() => {
      annotation.show();
    }, props.markDelay);
  }

  if (root.value && 
    ((props.hideMarkAt >= 0 && clicks.value >= props.hideMarkAt) || clicks.value <= props.markAt - 1)) {
    if (!annotation) return;
    if (!annotation.isShowing()) return;

    annotation.hide();
  }
}
</script>