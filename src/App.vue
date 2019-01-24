<template>
  <v-app>
    <v-content>
      <Sudoku/>
    </v-content>
  </v-app>
</template>

<script>
import Sudoku from './components/Sudoku'

export default {
  name: 'App',
  components: {
    Sudoku
  },
  data () {
    return {
      //
    }
  }
}
</script>
