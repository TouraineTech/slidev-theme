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
  <div class="slidev-layout cover" :class="[containerClass, { 'cover--light': !isDark }]">
    <div class="cover-content">
      <TntLogo size="xl" :inverted="isDark" class="cover-logo" />
      <div class="cover-text">
        <slot />
      </div>
    </div>
    <div class="cover-footer">
      <span class="cover-event">Touraine Tech</span>
    </div>
  </div>
</template>

<style scoped>
.cover {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: var(--tnt-primary, #222333);
  color: white;
  padding: 2rem;
  height: 100%;
  position: relative;
}

/* Light variant */
.cover--light {
  background: white;
  color: var(--tnt-primary, #222333);
}

.cover-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex: 1;
  text-align: center;
  gap: 2rem;
}

.cover-logo {
  margin-bottom: 1rem;
}

.cover-text {
  max-width: 80%;
}

.cover-text :deep(h1) {
  color: white;
  font-size: 3em;
  font-weight: 700;
  margin-bottom: 0.5em;
  line-height: 1.1;
}

.cover--light .cover-text :deep(h1) {
  color: var(--tnt-primary, #222333);
}

.cover-text :deep(h2),
.cover-text :deep(p) {
  color: var(--tnt-secondary, #6ABFAD);
  font-size: 1.5em;
  font-weight: 400;
  margin: 0;
}

.cover-footer {
  position: absolute;
  bottom: 2rem;
  right: 2rem;
  font-size: 0.9em;
  opacity: 0.7;
}

.cover-event {
  color: var(--tnt-secondary, #6ABFAD);
  font-weight: 500;
}

.cover--light .cover-event {
  color: var(--tnt-primary, #222333);
}
</style>
