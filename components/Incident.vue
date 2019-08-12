<template>
  <v-flex xs12 sm12 md3 pa-2>
    <v-card class="card-rounder elevation-0">
      <v-card-title primary-title>
        <v-avatar color="yellow" size="80">
          <img
            src="https://image.flaticon.com/icons/svg/1576/1576403.svg"
            alt="John"
            height="10"
            width="10"
          />
        </v-avatar>
      </v-card-title>
      <v-card-text>
        <h3 class="headline font-weight-light">{{ title }}</h3>
      </v-card-text>
    </v-card>
  </v-flex>
</template>

<script>
export default {
  name: 'CardEmployee',
  props: {
    image: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    lorem: {
      type: String,
      required: true
    }
  }
}
</script>

<style></style>
