/* eslint-disable no-console */
<template>
  <div dropzone="true">
    <v-card draggable="true" color="#3d3d3d" class="calculator">
      <div class="display">
        <v-text-field
          v-model="display"
          outlined
          label="Calculator"
          background-color="#858585"
        />
      </div>
      <div class="clear">
        <v-btn color="#fc5203" @click="clear">
          Clear
        </v-btn>
      </div>
      <div>
        <v-btn color="#9cff45" @click="div">
          /
        </v-btn>
      </div>
      <div>
        <v-btn color="#888888" @click="number('1')">
          1
        </v-btn>
      </div>
      <div>
        <v-btn color="#888888" @click="number('2')">
          2
        </v-btn>
      </div>
      <div>
        <v-btn color="#888888" @click="number('3')">
          3
        </v-btn>
      </div>
      <div>
        <v-btn color="#9cff45" @click="add">
          +
        </v-btn>
      </div>
      <div>
        <v-btn color="#888888" @click="number('4')">
          4
        </v-btn>
      </div>
      <div>
        <v-btn color="#888888" @click="number('5')">
          5
        </v-btn>
      </div>
      <div>
        <v-btn color="#888888" @click="number('6')">
          6
        </v-btn>
      </div>
      <div>
        <v-btn color="#9cff45" @click="Sub">
          -
        </v-btn>
      </div>
      <div>
        <v-btn color="#888888" @click="number('7')">
          7
        </v-btn>
      </div>
      <div>
        <v-btn color="#888888" @click="number('8')">
          8
        </v-btn>
      </div>
      <div>
        <v-btn color="#888888" @click="number('9')">
          9
        </v-btn>
      </div>
      <div>
        <v-btn color="#9cff45" @click="mul">
          x
        </v-btn>
      </div>
      <div class="zero">
        <v-btn color="#888888" @click="number('0')">
          0
        </v-btn>
      </div>
      <div>
        <v-btn color="#9cff45" @click="equals">
          =
        </v-btn>
      </div>
    </v-card>
  </div>
</template>
<script>
export default {
  data: () => ({
    display: '',
    result: '',
    getNumber: '',
    readInput: []
  }),
  methods: {
    number (val) {
      this.getNumber = this.getNumber + val
      this.display = this.display + val
    },
    clear () {
      this.display = ''
      this.result = ''
      this.getNumber = ''
    },
    add () {
      this.readInput.push(this.getNumber)
      this.display = this.display + '+'
      this.getNumber = ''
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
    equals () {
      this.result = ''
      this.readInput.push(this.getNumber)
      this.readInput.forEach((input) => {
        this.result = Number(this.result) + Number(input)
        this.display = '=' + this.result.toString()
        this.readInput = []
      })
    }
  }
}
</script>
<style scoped>
.calculator{
  margin: auto;
  width: 400px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(50px, auto);
}
.display {
  grid-column: 1/5;
}
.clear {
  grid-column: 1/4;
}
.zero {
 grid-column: 1/4;
}
</style>
