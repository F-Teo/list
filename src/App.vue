<template>
  <div id="app">
    <List v-bind:list='list' />
  </div>
</template>

<script>
import List from './components/List.vue'
import './assets/tailwind.css'

export default {
  name: 'App',
  components: {
    List
  },
  data: () => ({
    list: new Array(30).fill('').map((_, i) => ({
      index: i + 1,
      label: `Text ${i + 1}`,
      value: Math.round(Math.random() * 100),
    })),
  }),
}
</script>

<style>

</style>
