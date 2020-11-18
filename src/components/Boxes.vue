<template>
  <div id="boxes">
    <Box1 id="box" class="box1"/>
    <Box2 id="box" class="box2"/>
    <Box3 id="box" class="box3"/>
  </div>
</template>

<script>
import Box1 from './Box1.vue'
import Box2 from './Box2.vue'
import Box3 from './Box3.vue'

export default {
  name: 'App',
  components: {
    Box1,
    Box2,
    Box3
  }
}
</script>

<style>
#box {
  display: inline-block;
}
.box1{
    margin-left: 6%;
    width: 25vw;
}
.box2{
    width: 40vw;
}
.box3{
  width: 20vw;
}
</style>
