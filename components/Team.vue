<template>
  <v-flex xs12 sm12 md3 pa-4 text-xs-center>
    <v-card class="elevation-0 card-rounder">
      <v-card-title primary-title>
        <v-flex>
          <img
            src="https://image.flaticon.com/icons/svg/145/145859.svg"
            alt="location-pin"
            width="80"
          />
          <h1 class="title font-weight-regular">
            {{ name }}
          </h1>
          <h2 class="subheading font-weight-light ">{{ user }}</h2>
          <h2 class="subheading font-weight-light accent--text">
            {{ position }}
          </h2>
        </v-flex>
      </v-card-title>
    </v-card>
  </v-flex>
</template>

<script>
export default {
  name: 'Team',
  props: {
    name: {
      type: String,
      required: true
    },
    position: {
      type: String,
      required: true
    },
    user: {
      type: String,
      required: true
    }
  }
}
</script>

<style></style>
