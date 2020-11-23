<template>
  <div id="app">
    <Boxes/>
    <PianoRoll/>
  </div>
</template>

<script>
import Boxes from './components/Boxes.vue'
import PianoRoll from './components/PianoRoll.vue'

export default {
  name: 'App',
  components: {
    Boxes,
    PianoRoll
  }
}
</script>

<style>
</style>
