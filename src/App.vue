<script setup>
import { ref } from 'vue'
import InputComponent from './components/InputComponent.vue';
const msg = ref('message there you are!')
const count = ref(0)
const increment = () => {
  count.value++
}
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <h1>{{ msg }}</h1>
      <button @click="increment">press me and will count: {{ count }}</button>

    </div>
  </header>

  <main>
    <InputComponent />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
