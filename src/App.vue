<template>
  <v-app>
    <v-main>
      <HelloWorld/>
    </v-main>
    <v-row
        align="center"
        justify="center"
    >
      <v-card
          height="300"
          width="250"
      >
        <v-row justify="center">
          <v-btn
              color="success"
              class="mt-12"
              @click="overlay = !overlay"
          >
            Show Overlay
          </v-btn>

          <v-overlay
              :absolute="absolute"
              v-model="overlay"
          >
            <v-btn
                color="success"
                @click="overlay = false"
            >
              Hide Overlay
            </v-btn>
          </v-overlay>
        </v-row>
      </v-card>
    </v-row>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    absolute: true,
    overlay: false,
  }),
}
</script>
