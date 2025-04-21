<script setup>
import { defineProps, h } from 'vue'
import * as icons from 'lucide-vue-next'

const props = defineProps({
  name: {
    type: String,
    required: true
  },
  size: {
    type: [String, Number],
    default: 16
  },
  color: {
    type: String,
    default: 'currentColor'
  }
})

const IconComponent = icons[props.name]
</script>

<template>
  <span class="icon-wrapper">
    <IconComponent v-if="IconComponent" :size="size" :color="color" />
    <span v-else>Icon not found: {{ name }}</span>
  </span>
</template>

<style>
.icon-wrapper {
  display: inline-flex;
  align-items: center;
  vertical-align: middle;
  position: relative;
  top: -0.05em;
}
</style> 