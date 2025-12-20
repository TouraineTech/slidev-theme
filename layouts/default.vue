<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{
  class?: string
}>()

const containerClass = computed(() => props.class)
</script>

<template>
  <div class="slidev-layout default" :class="containerClass">
    <div class="default-content">
      <slot />
    </div>
    <div class="default-footer">
      <TntLogo size="sm" inverted />
    </div>
  </div>
</template>

<style scoped>
.default {
  display: flex;
  flex-direction: column;
  padding: 2.5rem 3rem;
  height: 100%;
  position: relative;
  background: var(--tnt-primary, #222333);
  color: white;
}

.default-content {
  flex: 1;
  overflow: auto;
}

.default-content :deep(h1) {
  color: white;
  font-size: 2.2em;
  font-weight: 700;
  margin-bottom: 1em;
  padding-bottom: 0.3em;
  border-bottom: 3px solid var(--tnt-secondary, #6ABFAD);
}

.default-content :deep(h2) {
  color: white;
  font-size: 1.6em;
  font-weight: 600;
  margin-top: 1em;
  margin-bottom: 0.5em;
}

.default-content :deep(ul),
.default-content :deep(ol) {
  font-size: 1.2em;
  line-height: 1.6;
}

.default-content :deep(p) {
  font-size: 1.2em;
  line-height: 1.6;
}

.default-footer {
  position: absolute;
  bottom: 1.5rem;
  right: 2rem;
  opacity: 0.6;
  transition: opacity 0.2s ease;
}

.default-footer:hover {
  opacity: 1;
}

/* Dark mode */
html.dark .default-content :deep(h1),
html.dark .default-content :deep(h2) {
  color: white;
}
</style>
