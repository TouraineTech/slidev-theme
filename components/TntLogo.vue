<script setup lang="ts">
defineProps<{
  size?: 'sm' | 'md' | 'lg' | 'xl'
  inverted?: boolean
}>()
</script>

<template>
  <div class="tnt-logo" :class="[`tnt-logo--${size ?? 'md'}`, { 'tnt-logo--inverted': inverted }]">
    <svg viewBox="0 0 416 176" xmlns="http://www.w3.org/2000/svg">
      <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
        <g transform="translate(-238.000000, -58.000000)">
          <g transform="translate(238.000000, 58.000000)">
            <!-- T droite -->
            <g transform="translate(240.000000, 0.000000)">
              <rect class="tnt-primary" x="60" y="120" width="56" height="56" />
              <rect class="tnt-primary" x="60" y="60" width="56" height="56" />
              <rect class="tnt-primary" x="60" y="0" width="56" height="56" />
              <rect class="tnt-primary" x="0" y="0" width="56" height="56" />
              <rect class="tnt-primary" x="120" y="0" width="56" height="56" />
              <polygon class="tnt-secondary" points="0 0 56 56 0 56" />
            </g>
            <!-- N -->
            <g transform="translate(120.000000, 60.000000)" class="tnt-secondary">
              <rect x="0" y="0" width="56" height="56" />
              <rect x="0" y="60" width="56" height="56" />
              <polygon points="60 60 116 60 116 116" />
              <polygon points="60 0 116 56 60 56" />
              <rect x="120" y="0" width="56" height="56" />
              <rect x="120" y="60" width="56" height="56" />
            </g>
            <!-- T gauche -->
            <g class="tnt-primary">
              <rect x="60" y="120" width="56" height="56" />
              <rect x="60" y="60" width="56" height="56" />
              <rect x="60" y="0" width="56" height="56" />
              <rect x="0" y="0" width="56" height="56" />
              <rect x="120" y="0" width="56" height="56" />
            </g>
            <polygon class="tnt-secondary" points="120 0 176 56 120 56" />
          </g>
        </g>
      </g>
    </svg>
  </div>
</template>

<style scoped>
.tnt-logo {
  display: inline-flex;
  align-items: center;
  justify-content: center;
}

.tnt-logo svg {
  width: 100%;
  height: auto;
}

/* Sizes */
.tnt-logo--sm {
  width: 80px;
}

.tnt-logo--md {
  width: 150px;
}

.tnt-logo--lg {
  width: 250px;
}

.tnt-logo--xl {
  width: 400px;
}

/* Colors */
.tnt-primary {
  fill: #222333;
}

.tnt-secondary {
  fill: #6ABFAD;
}

/* Inverted mode for dark backgrounds */
.tnt-logo--inverted .tnt-primary {
  fill: #ffffff;
}
</style>
