<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{
  class?: string
  variant?: 'dark' | 'light'
}>()

const containerClass = computed(() => props.class)
const isDark = computed(() => props.variant !== 'light')
</script>

<template>
  <div class="slidev-layout section" :class="[containerClass, { 'section--light': !isDark }]">
    <div class="section-content">
      <slot />
    </div>
    <div class="section-decoration">
      <div class="triangle triangle-1"></div>
      <div class="triangle triangle-2"></div>
    </div>
  </div>
</template>

<style scoped>
.section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: var(--tnt-primary, #222333);
  color: white;
  padding: 3rem;
  height: 100%;
  position: relative;
  overflow: hidden;
}

/* Light variant */
.section--light {
  background: white;
  color: var(--tnt-primary, #222333);
}

.section-content {
  text-align: center;
  z-index: 1;
}

.section-content :deep(h1) {
  color: white;
  font-size: 3.5em;
  font-weight: 700;
  margin: 0;
  line-height: 1.2;
}

.section--light .section-content :deep(h1) {
  color: var(--tnt-primary, #222333);
}

.section-content :deep(h2),
.section-content :deep(p) {
  color: var(--tnt-secondary, #6ABFAD);
  font-size: 1.5em;
  font-weight: 400;
  margin-top: 0.5em;
}

/* Decorative triangles inspired by TNT logo */
.section-decoration {
  position: absolute;
  inset: 0;
  pointer-events: none;
}

.triangle {
  position: absolute;
  width: 0;
  height: 0;
  border-style: solid;
}

.triangle-1 {
  bottom: 0;
  left: 0;
  border-width: 0 0 150px 150px;
  border-color: transparent transparent var(--tnt-secondary, #6ABFAD) transparent;
  opacity: 0.3;
}

.section--light .triangle-1 {
  opacity: 0.5;
}

.triangle-2 {
  top: 0;
  right: 0;
  border-width: 100px 100px 0 0;
  border-color: var(--tnt-secondary, #6ABFAD) transparent transparent transparent;
  opacity: 0.2;
}

.section--light .triangle-2 {
  opacity: 0.4;
}
</style>
