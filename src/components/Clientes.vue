<template>
  <v-container fluid>
    <v-row align="left">
      <v-col
        class="d-flex"
        cols="12"
        sm="6"
      >
        <v-select
          :items="items1"
          label="Todos los clientes"
          dense
          outlined
          class="clientes"
        />
        <v-select
          :items="items2"
          label="Todos los proyectos"
          dense
          outlined
        />
      </v-col>
    </v-row>
    <v-row align="left">
      <v-col
        class="d-flex"
        cols="12"
        sm="2"
      >
        <v-select
          :items="items3"
          label="Datos generales"
          dense
          outlined
        />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'Clientes',

    data: () => ({
      items1: ['Cliente1', 'Cliente2', 'Cliente3', 'Cliente4'],
      items2: ['Proyecto1', 'Proyecto2', 'Proyecto3', 'Proyecto4'],
      items3: ['Vista1', 'Vista2', 'Vista3', 'Vista4'],
    }),
  }
</script>

<style lang="sass" scoped>
  a
    color: inherit !important
  .clientes
    margin-right: 10px !important
</style>
