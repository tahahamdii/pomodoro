<template>
  <v-app>
    <v-main>
      <v-container>
        <v-row>
          <v-col sm="6" offset-sm="3">
            <PomodoroTimer :dialog="dialog" :closeDialog="closeDialog" />
          </v-col>
          <v-btn
            @click="dialog = true"
            color="secondary"
            dark
            small
            top
            right
            fab
          >
            <v-icon>mdi-cog-outline</v-icon>
          </v-btn>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import PomodoroTimer from './components/PomodoroTimer';
export default {
  name: 'App',
  components: {
    PomodoroTimer,
  },
  data() {
    return {
      dialog: false
    }
  },
  methods: {
    closeDialog() {
      this.dialog = false
    }
  }
};
</script>
