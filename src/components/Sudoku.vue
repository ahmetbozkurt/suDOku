<template>
  <v-data-table
    :items="desserts"
    class="elevation-1"
    hide-actions
    hide-headers
  >
    <template slot="items" slot-scope="props" >

    <td> <v-text-field v-model="props.item.A"></v-text-field> </td>
    <td> <v-text-field v-model="props.item.B"></v-text-field> </td>
    <td> <v-text-field v-model="props.item.C"></v-text-field> </td>
    <td> <v-text-field v-model="props.item.D"></v-text-field> </td>
    <td> <v-text-field v-model="props.item.E"></v-text-field> </td>
    <td> <v-text-field v-model="props.item.F"></v-text-field> </td>
    <td> <v-text-field v-model="props.item.G"></v-text-field> </td>
    <td> <v-text-field v-model="props.item.H"></v-text-field> </td>
    <td> <v-text-field v-model="props.item.I"></v-text-field> </td>
  
    </template>
  </v-data-table>
</template>

<style>
td {
  height:30px;
  width:30px;
  border:1px solid;
  text-align:center;
}
td:first-child {
  border-left:solid;
}
td:nth-child(3n) {
  border-right:solid ;
}
tr:first-child {
  border-top:solid;
}
tr:nth-child(3n) td {
  border-bottom:solid ;
}

table {
  margin:1em auto;
}
</style>

<script>
  export default {
    data () {
      return {
        desserts: [
          {
            A: "1",
            B: "1",
            C: "1",
            D: "1",
            E: "1",
            F: "1",
            G: "1",
            H: "1",
            I: "1",
            ColNumber : "1"
          },
          {
            A: "1",
            B: "1",
            C: "1",
            D: "1",
            E: "1",
            F: "1",
            G: "1",
            H: "1",
            I: "1",
            ColNumber : "2"
          },         
          {
            A: "1",
            B: "1",
            C: "1",
            D: "1",
            E: "1",
            F: "1",
            G: "1",
            H: "1",
            I: "1",
            ColNumber : "3"
          },          
          {
            A: "1",
            B: "1",
            C: "1",
            D: "1",
            E: "1",
            F: "1",
            G: "1",
            H: "1",
            I: "1",
            ColNumber : "4"
          },          
          {
            A: "1",
            B: "1",
            C: "1",
            D: "1",
            E: "1",
            F: "1",
            G: "1",
            H: "1",
            I: "1",
            ColNumber : "5"
          },          
          {
            A: "1",
            B: "1",
            C: "1",
            D: "1",
            E: "1",
            F: "1",
            G: "1",
            H: "1",
            I: "1",
            ColNumber : "6"
          },          
          {
            A: "1",
            B: "1",
            C: "1",
            D: "1",
            E: "1",
            F: "1",
            G: "1",
            H: "1",
            I: "1",
            ColNumber : "7"
          },          
          {
            A: "1",
            B: "1",
            C: "1",
            D: "1",
            E: "1",
            F: "1",
            G: "1",
            H: "1",
            I: "1",
            ColNumber : "8"
          },          
          {
            A: "1",
            B: "1",
            C: "1",
            D: "1",
            E: "1",
            F: "1",
            G: "1",
            H: "1",
            I: "1",
            ColNumber : "9"
          },
        ]
      }
    }
  }
</script>