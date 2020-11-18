<template>
  <div class="btn-group">

        <form>
            <label for="scale">Choose scale: </label>
            <br>
            <select name="scale" id="scale">
                <option value="Minor">Minor</option>
                <option value="Major">Major</option>
            </select>
        </form>

        <form>
            <label for="key">Choose key: </label>
            <br>
            <select name="key" id="key">
                <option value="B">B</option>
                <option value="A#">A#</option>
                <option value="A">A</option>
                <option value="G#">G#</option>
                <option value="G">G</option>
                <option value="F#">F#</option>
                <option value="F">F</option>
                <option value="E">E</option>
                <option value="D#">D#</option>
                <option value="D">D</option>
                <option value="C#">C#</option>
                <option value="C">C</option>
            </select>
        </form>

        <form>
            <label for="harmonicFunction">Choose harmonic function: </label>
            <br>
            <select name="harmonicFunction" id="harmonicFunction">
                <option value="harmonicTriad">Harmonic triad</option>
            </select>
        </form>

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
form {
    display:inline-block;
    margin-left: 1%;
}
</style>
