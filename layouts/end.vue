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
  <div class="slidev-layout end" :class="[containerClass, { 'end--light': !isDark }]">
    <div class="end-content">
      <TntLogo size="xl" :inverted="isDark" class="end-logo" />
      <div class="end-text">
        <slot>
          <h1>Merci !</h1>
          <p>Des questions ?</p>
        </slot>
      </div>
    </div>
    <div class="end-links">
      <a href="https://touraine.tech" target="_blank" rel="noopener">touraine.tech</a>
      <span class="separator">|</span>
      <a href="https://x.com/tourainetech" target="_blank" rel="noopener">@tourainetech</a>
    </div>
    <div class="end-decoration">
      <div class="triangle triangle-1"></div>
      <div class="triangle triangle-2"></div>
      <div class="triangle triangle-3"></div>
    </div>
  </div>
</template>

<style scoped>
.end {
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
.end--light {
  background: white;
  color: var(--tnt-primary, #222333);
}

.end-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex: 1;
  text-align: center;
  z-index: 1;
  gap: 2rem;
}

.end-logo {
  margin-bottom: 1rem;
}

.end-text :deep(h1) {
  color: white;
  font-size: 3.5em;
  font-weight: 700;
  margin: 0;
}

.end--light .end-text :deep(h1) {
  color: var(--tnt-primary, #222333);
}

.end-text :deep(p) {
  color: var(--tnt-secondary, #6ABFAD);
  font-size: 1.8em;
  margin-top: 0.5em;
}

.end-links {
  position: absolute;
  bottom: 2rem;
  display: flex;
  gap: 1rem;
  align-items: center;
  z-index: 1;
}

.end-links a {
  color: var(--tnt-secondary, #6ABFAD);
  text-decoration: none;
  font-size: 1.1em;
  transition: color 0.2s ease;
}

.end-links a:hover {
  color: white;
}

.end--light .end-links a:hover {
  color: var(--tnt-primary, #222333);
}

.separator {
  color: rgba(255, 255, 255, 0.3);
}

.end--light .separator {
  color: rgba(34, 35, 51, 0.3);
}

/* Decorative triangles */
.end-decoration {
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
  border-width: 0 0 200px 200px;
  border-color: transparent transparent var(--tnt-secondary, #6ABFAD) transparent;
  opacity: 0.2;
}

.end--light .triangle-1 {
  opacity: 0.4;
}

.triangle-2 {
  top: 0;
  right: 0;
  border-width: 150px 150px 0 0;
  border-color: var(--tnt-secondary, #6ABFAD) transparent transparent transparent;
  opacity: 0.15;
}

.end--light .triangle-2 {
  opacity: 0.3;
}

.triangle-3 {
  bottom: 100px;
  right: 50px;
  border-width: 0 0 80px 80px;
  border-color: transparent transparent var(--tnt-secondary, #6ABFAD) transparent;
  opacity: 0.1;
}

.end--light .triangle-3 {
  opacity: 0.2;
}
</style>
