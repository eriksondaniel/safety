<template>
  <v-flex xs12 sm8 offset-sm2>
    <v-card class="card-rounder">
      <!-- <v-card-title primary-title>
        <div>
          <div class="headline">Top western road trips</div>
          <span class="grey--text">1,000 miles of wonder</span>
        </div>
      </v-card-title> -->
      <v-card-actions>
        <h2 class="subheading font-weight-medium">{{ question }}</h2>
        <v-spacer></v-spacer>
        <v-btn icon @click.native="show = !show">
          <v-icon color="red">
            {{ show ? 'keyboard_arrow_down' : 'keyboard_arrow_up' }}
          </v-icon>
        </v-btn>
      </v-card-actions>
      <v-slide-y-transition>
        <v-card-text v-show="show">
          {{ response }}
        </v-card-text>
      </v-slide-y-transition>
    </v-card>
  </v-flex>
</template>

<script>
export default {
  name: 'CardEmployee',
  props: {
    question: {
      type: String,
      required: true
    },
    response: {
      type: String,
      required: true
    }
  },
  data: () => ({
    show: false
  })
}
</script>

<style></style>
