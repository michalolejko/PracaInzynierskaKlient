<template>
  <div class="btn-group">
    <button id=playBtn title="Play"></button>
    <button id=stopBtn title="Stop"></button>
    <input type="number" id="BpmInput" title="Tempo in BPM. It must be higher than 30, and lower than 300."
      onchange="if(this.value > 300) this.value = 300; if(this.value < 30) this.value = 30"
       min="30" max="300" value="100">
  </div>
</template>

<script>
export default {
  name: 'Box1',
  props: {
  },

methods:{
  
}
};

</script>

<style scoped>
button, input{
    display:inline-block;
    margin-left: 1%;
}
input#BpmInput{
  box-sizing: border-box;
  width: 52px;
  height: 22px;
  position: relative;
  bottom: 4px;
}
button#stopBtn{
  box-sizing: border-box;
    transform: scale(var(--ggs,1));
    width: 26px;
    height: 22px
}
button#stopBtn::before {
    content: "";
    display: block;
    box-sizing: border-box;
    width: 0;
    height: 10px;
    border-top: 0px solid transparent;
    border-left: 10px solid;
    top: 6px;
    left: 9px
}
button#playBtn{
  box-sizing: border-box;
    transform: scale(var(--ggs,1));
    width: 26px;
    height: 22px
}
button#playBtn::before {
    content: "";
    display: block;
    box-sizing: border-box;
    width: 0px;
    height: 10px;
    border-top: 5px solid transparent;
    border-bottom: 5px solid transparent;
    border-left: 10px solid;
    top: 6px;
    left: 9px
}
</style>
