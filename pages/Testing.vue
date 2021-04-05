<template>
  <v-card
    color="red"
    height="100px"
    width="auto"
  >
    <v-row
      justify="center"
      align="center"
    >
      <v-col
        cols="11"
      >
        <v-text-field
          v-model="display"
          outlined
          background-color="yellow"
          color="info"
          label="Display"
        />
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    num1: [],
    num2: [],
    nums: ''
  }),
  methods: {}
}
</script>
