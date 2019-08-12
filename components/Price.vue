<template>
  <v-flex xs12 sm12 md3>
    <v-card class="card-rounder elevation-24">
      <v-card-title primary-title>
        <div>
          <h3 class="headline mb-0">{{ title }}</h3>
          <h1>{{ price }}</h1>
        </div>
      </v-card-title>
      <v-divider inset />
      <v-card-text>
        <p>Caracteristica 1</p>
        <p>Caracteristica 2</p>
        <p>Caracteristica 3</p>
        <p>Caracteristica 4</p>
        <p>Caracteristica 5</p>
      </v-card-text>
      <v-card-actions>
        <v-btn flat color="primary">EMPIEZA AHORA</v-btn>
      </v-card-actions>
    </v-card>
  </v-flex>
</template>

<script>
export default {
  name: 'Price',
  props: {
    price: {
      type: Number,
      required: true
    },
    title: {
      type: String,
      required: true
    }
  }
}
</script>

<style></style>
