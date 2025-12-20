<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{
  class?: string
}>()

const containerClass = computed(() => props.class)
</script>

<template>
  <div class="slidev-layout two-cols" :class="containerClass">
    <div class="two-cols-container">
      <div class="col col-left">
        <slot name="default" />
      </div>
      <div class="col col-right">
        <slot name="right" />
      </div>
    </div>
    <div class="two-cols-footer">
      <TntLogo size="sm" inverted />
    </div>
  </div>
</template>

<style scoped>
.two-cols {
  display: flex;
  flex-direction: column;
  padding: 2.5rem 3rem;
  height: 100%;
  position: relative;
  background: var(--tnt-primary, #222333);
  color: white;
}

.two-cols-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  flex: 1;
  overflow: auto;
}

.col {
  display: flex;
  flex-direction: column;
}

.col :deep(h1) {
  color: white;
  font-size: 2em;
  font-weight: 700;
  margin-bottom: 0.8em;
  padding-bottom: 0.3em;
  border-bottom: 3px solid var(--tnt-secondary, #6ABFAD);
}

.col :deep(h2) {
  color: white;
  font-size: 1.4em;
  font-weight: 600;
  margin-top: 0.8em;
  margin-bottom: 0.4em;
}

.col :deep(ul),
.col :deep(ol) {
  font-size: 1.1em;
  line-height: 1.5;
}

.col :deep(p) {
  font-size: 1.1em;
  line-height: 1.5;
}

.col :deep(img) {
  max-width: 100%;
  height: auto;
  border-radius: 8px;
}

.two-cols-footer {
  position: absolute;
  bottom: 1.5rem;
  right: 2rem;
  opacity: 0.6;
  transition: opacity 0.2s ease;
}

.two-cols-footer:hover {
  opacity: 1;
}

/* Dark mode */
html.dark .col :deep(h1),
html.dark .col :deep(h2) {
  color: white;
}
</style>
