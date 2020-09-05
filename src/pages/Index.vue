<template>
  <q-page class="flex flex-center">
    <img alt="Quasar logo" src="~assets/quasar-logo-full.svg" />
    <div class="q-pa-md">
      <div class="row q-gutter">
        <div class="col col-md-4 col-sm-12"
        v-for="character in characters"
        :key="character.id"
        >
        <q-card dark bordered class="bg-grey-9 my-card">
          <q-card-section>
            <img :src="character.imagen" alt="">
          </q-card-section>
           <q-separator dark inset />
          <q-card-section>
            <q-card-title>{{ character.nombre }}</q-card-title>
          </q-card-section>
        </q-card>

        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex",
  data() {
    return {
      characters: [
        {
          id: 1,
          nombre: "Morty",
          imagen: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
        },
        {
          id: 2,
          nombre: "Rick",
          imagen: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
        },
        {
          id: 3,
          nombre: "Summer",
          imagen: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
        },
        {
          id: 4,
          nombre: "Beth",
          imagen: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
        },
        {
          id: 5,
          nombre: "Jerry",
          imagen: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
        },
      ],
    };
  },
};
</script>
