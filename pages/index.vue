<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <div class="text-center">
        <logo />
        <vuetify-logo />
      </div>
      <v-card>
        <v-card-title class="headline">
          Welcome to My First App
        </v-card-title>
        <v-card-text>
          <p>This is a calculator App</p>
          <p>
            Follow the link to the app<a
              href="https://localhost:3000/Calculator/"
              target="_blank"
              rel="noopener noreferrer"
            >
              Calculator
            </a>.
          </p>
          <p>
            This is my app under construction<a
              href="https://localhost:3000/CalculatorAD/"
              target="_blank"
              rel="noopener noreferrer"
              title="chat"
            >
              this is the app
            </a>.
          </p>
          <div class="text-xs-right">
            <em><small>&mdash; Amaan</small></em>
          </div>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/inspire"
          >
            Continue
          </v-btn>
          <v-btn
            color="primary"
            nuxt
            to="/Calculator"
          >
            Calculator
          </v-btn>
          <v-btn
            color="primary"
            nuxt
            to="/CalculatorAD"
          >
            Calculator-AD
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  }
}
</script>
