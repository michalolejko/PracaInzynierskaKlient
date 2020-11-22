<template>
  <div class="container">
    <br />
    <table class="table table-striped table-bordered">
      <thead>
        <tr>
          <th></th>
          <th>1</th>
          <th>2</th>
          <th>3</th>
          <th>4</th>
          <th>5</th>
          <th>6</th>
          <th>7</th>
          <th>8</th>
        </tr>
      </thead>
      <tbody >
        <tr v-for="area in areas" :key="area.id">
          <td id="firstCol">{{ area.note }}</td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      areas: [
        { note: "B" },
        { note: "A#" },
        { note: "A" },
        { note: "G#" },
        { note: "G" },
        { note: "F#" },
        { note: "F" },
        { note: "E" },
        { note: "D#" },
        { note: "D" },
        { note: "C#" },
        { note: "C" },
      ],
    };
  },
};
</script>

<style>
table,
td {
  border: 1px solid black;
  width: 100%;
}
table {
  border-collapse: collapse;
  table-layout: fixed;
}
td {
  height: 20px;
}
td:hover {
  background-color: blue;
}
#firstCol {
  border: 0px;
}
</style>
