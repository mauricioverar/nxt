<!-- Please remove this file from your project -->
<template>
  <v-app>
    <v-container class="fill-height" fluid style="min-height: 434px">
      <v-fade-transition mode="out-in">
        <v-row class="row px-16">
          <v-col v-for="(item, index) in personajes" :key="index" cols="4">
            <v-card>
              <v-img
                :src="item.imagen"
                height="420"
                class="grey darken-4"
              />
              <v-card-title class="text-h6">
                {{ item.nombre }}
              </v-card-title>
            </v-card>
          </v-col>
        </v-row>
      </v-fade-transition>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  data () {
    return {
      personajes: [
        {
          id: 1,
          nombre: 'Morty',
          imagen:
          'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
        },
        {
          id: 2,
          nombre: 'Rick',
          imagen:
          'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
        },
        {
          id: 3,
          nombre: 'Summer',
          imagen:
          'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
        },
        {
          id: 4,
          nombre: 'Beth',
          imagen:
          'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
        },
        {
          id: 5,
          nombre: 'Jerry',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
        }
      ]
    }
  }
}
</script>
