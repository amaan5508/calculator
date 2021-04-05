<template>
  <v-form
    ref="form"
    v-model="valid"
    lazy-validation
  >
    <v-text-field
      v-model="value_1"
      label="Value-1"
      required
    />

    <v-text-field
      v-model="value_2"
      label="Value-2"
      required
    />

    <v-text-field
      v-model="result"
      label="Result"
    />

    <v-btn
      color="success"
      class="mr-4"
      @click="Add"
    >
      Add
    </v-btn>

    <v-btn
      color="success"
      class="mr-4"
      @click="Multiplication"
    >
      Multiplication
    </v-btn>

    <v-btn
      color="success"
      class="mr-4"
      @click="Subtraction"
    >
      Subtraction
    </v-btn>

    <v-btn
      color="success"
      class="mr-4"
      @click="Division"
    >
      Division
    </v-btn>

    <v-btn
      color="error"
      class="mr-4"
      @click="reset"
    >
      Reset
    </v-btn>
  </v-form>
</template>

<script>
export default {
  data: () => ({
    Value_1: 0,
    Value_2: 0,
    result: 0
  }),

  methods: {
    Add () { this.result = Number(this.value_1) + Number(this.value_2) },
    Subtraction () { this.result = Number(this.value_1) - Number(this.value_2) },
    Multiplication () { this.result = Number(this.value_1) * Number(this.value_2) },
    Division () { this.result = Number(this.value_1) / Number(this.value_2) },
    reset () { this.$refs.form.reset() }
  }
}
</script>
