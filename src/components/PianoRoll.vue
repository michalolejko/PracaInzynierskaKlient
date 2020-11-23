<template>
  <div class="container">
    <br />
    <table class="table table-striped table-bordered">
      <thead>
        <tr>
          <th></th>
          <th v-for="area in areas" :key="area.id">{{ area.no }}</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(note, note_index) in notes" :key="note.id" :num-labels="40">
          <td id="firstCol">{{ note.note }}</td>
          <td
            v-for="(area, area_index) in areas"
            :key="area.id"
            v-bind:id="note.note + area.no"
            
            @click="fieldClicked(note_index, area_index, note.note + area.no)"
          ></td><!-- @contextmenu.prevent="rightClickHandler" -mozna tutaj dodac na prawym kliku np wyczysc wszystko i dac to do "td" np nad @click=fieldClicked-->
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      notes: [
        { note: "B4" },
        { note: "A#4" },
        { note: "A4" },
        { note: "G#4" },
        { note: "G4" },
        { note: "F#4" },
        { note: "F4" },
        { note: "E4" },
        { note: "D#4" },
        { note: "D4" },
        { note: "C#4" },
        { note: "C4" },
        { note: "B3" },
        { note: "A#3" },
        { note: "A3" },
        { note: "G#3" },
        { note: "G3" },
        { note: "F#3" },
        { note: "F3" },
        { note: "E3" },
        { note: "D#3" },
        { note: "D3" },
        { note: "C#3" },
        { note: "C3" },
        { note: "B2" },
        { note: "A#2" },
        { note: "A2" },
        { note: "G#2" },
        { note: "G2" },
        { note: "F#2" },
        { note: "F2" },
        { note: "E2" },
        { note: "D#2" },
        { note: "D2" },
        { note: "C#2" },
        { note: "C2" },
        { note: "B1" },
        { note: "A#1" },
        { note: "A1" },
        { note: "G#1" },
        { note: "G1" },
        { note: "F#1" },
        { note: "F1" },
        { note: "E1" },
        { note: "D#1" },
        { note: "D1" },
        { note: "C#1" },
        { note: "C1" },
      ],
      areas: [
        { no: 1 },
        { no: 2 },
        { no: 3 },
        { no: 4 },
        { no: 5 },
        { no: 6 },
        { no: 7 },
        { no: 8 },
        { no: 9 },
        { no: 10 },
        { no: 11 },
        { no: 12 },
        { no: 13 },
        { no: 14 },
        { no: 15 },
        { no: 16 },
      ],
    };
  },
  methods: {
    fieldClicked(note_index, area_index, id) {
      let area = this.areas[area_index];
      let note = this.notes[note_index];
      let field = document.getElementById(id);
      console.log(note.note, area.no);

      if (
        field.style.backgroundColor == "white" ||
        field.style.backgroundColor == ""
      ) {
        field.style.backgroundColor = "blue";
      } else {
        field.style.backgroundColor = "white";
      }
    },

  },
};
</script>

<style>
table,
td {
  border: 1px solid black;
  width: 100%;
  border-radius: 15%;
}
table {
  border-collapse: collapse;
  table-layout: fixed;
  width: 100%;
}
tbody td,
thead th {
  width: 20%; /* Optional */
}
td:hover {
  background-color: rgba(0, 0, 255, 0.5);
}
#firstCol {
  border: 0px;
  width: 50px;
}
#firstCol:hover {
  background-color: white;
}
</style>