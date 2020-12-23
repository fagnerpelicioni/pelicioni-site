<template>
  <v-row class="main-section" justify="center" align="center">
    <section class="main">
      <h1 class="reveal-text">
        {{ $t('coming_soon') }}
      </h1>
    </section>
  </v-row>
</template>

<script>
export default {
  name: 'BlogPage',

  layout: 'landing',

  transition: 'slide-bottom'
}
</script>

<style lang="scss" scoped>
:root {
  --delay: 0;
  --duration: 800ms;
  --iterations: 1;
}

.main {
  padding-top: 4rem;
}

.reveal-text,
.reveal-text::after {
  animation-delay: var(--animation-delay, 2s);
  animation-iteration-count: var(--iterations, 1);
  animation-duration: var(--duration, 800ms);
  animation-fill-mode: both;
  animation-timing-function: cubic-bezier(0.0, 0.0, 0.2, 1);
}

.reveal-text {
  --animation-delay: var(--delay, 0);
  --animation-duration: var(--duration, 800ms);
  --animation-iterations: var(--iterations, 1);
  position: relative;
  font-size: 16px;
  font-family: $montserrat;
  animation-name: clip-text;
  color: var(--v-accent-base);
  font-weight: $font-regular;
  white-space: nowrap;
  cursor: default;

  &::after {
    content: "";
    position: absolute;
    z-index: 999;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: $primary;
    transform: scaleX(0);
    transform-origin: 0 50%;
    pointer-events: none;
    animation-name: text-revealer;
  }

}

@keyframes clip-text {
  from {
    clip-path: inset(0 100% 0 0);
  }
  to {
    clip-path: inset(0 0 0 0);
  }
}

@keyframes text-revealer {

  0%, 50% {
    transform-origin: 0 50%;
  }

  60%, 100% {
    transform-origin: 100% 50%;
  }

  60% {
    transform: scaleX(1);
  }

  100% {
    transform: scaleX(0);
  }
}
</style>
