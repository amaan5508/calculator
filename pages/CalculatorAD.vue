/* eslint-disable no-console */
<template>
  <v-card
    justify="center"
    align="center"
    class="pb-4"
    min-height="450px"
    height="auto"
    width="550px"
    elevation="5"
  >
    <v-row
      justify="center"
      align="center"
      no-gutters
      style="height: 150px;"
    >
      <v-col
        cols="8"
        sm="8"
      >
        <v-text-field
          v-model="display"
          outlined
          label="Calculator"
        />
        <v-btn
          color="yellow darken-4"
          elevation="6"
          x-large
          @click="number('1')"
        >
          1
        </v-btn>
        <v-btn
          color="yellow darken-4"
          elevation="6"
          x-large
          @click="number('2')"
        >
          2
        </v-btn>
        <v-btn
          color="yellow darken-4"
          elevation="6"
          x-large
          @click="number('3')"
        >
          3
        </v-btn>
        <v-btn
          elevation="6"
          x-large
          color="success"
          @click="add"
        >
          +
        </v-btn>
        <v-btn
          color="yellow darken-4"
          elevation="6"
          x-large
          @click="number('4')"
        >
          4
        </v-btn>
        <v-btn
          color="yellow darken-4"
          elevation="6"
          x-large
          @click="number('5')"
        >
          5
        </v-btn>
        <v-btn
          color="yellow darken-4"
          elevation="6"
          x-large
          @click="number('6')"
        >
          6
        </v-btn>
        <v-btn
          elevation="6"
          x-large
          color="success"
          @click="Sub"
        >
          -
        </v-btn>
        <v-btn
          color="yellow darken-4"
          elevation="6"
          x-large
          @click="number('7')"
        >
          7
        </v-btn>
        <v-btn
          color="yellow darken-4"
          elevation="6"
          x-large
          @click="number('8')"
        >
          8
        </v-btn>
        <v-btn
          color="yellow darken-4"
          elevation="6"
          x-large
          @click="number('9')"
        >
          9
        </v-btn>
        <v-btn
          elevation="6"
          x-large
          color="success"
          @click="div"
        >
          /
        </v-btn>
        <v-btn
          color="orange darken-4"
          elevation="6"
          x-large
          style="width: 285px"
          @click="'0'"
        >
          0
        </v-btn>
        <v-btn
          elevation="6"
          x-large
          color="success"
          @click="mul"
        >
          x
        </v-btn>
        <v-btn
          color="error"
          x-large
          @click="clear"
        >
          Clear
        </v-btn>
      </v-col>
      <v-text-field
        v-model="result"
        label="Result"
        color=""
      />
      <div>
        <v-btn
          color="success"
          x-small
          @click="give"
        >
          ok
        </v-btn>
      </div>
    </v-row>
  </v-card>
</template>
<script>
export default {
  data: () => ({
    display: '',
    result: ''
  }),
  watch: () => ({
    display: (value) => { console.log(this.display) }
  }),
  methods: {
    number (val) {
      this.display = this.display + val
    },
    clear () {
      this.display = ''
      this.result = ''
    },
    add () {
      this.display = this.display + '+'
    },
    Sub () {
      this.display = this.display + '-'
    },
    mul () {
      this.display = this.display + 'x'
    },
    div () {
      this.display = this.display + '/'
    },
    give () {
    }
  }
}
</script>
