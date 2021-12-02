<template>
  <v-card>
    <v-card-title>
      <v-btn>
        <v-icon left>mdi-plus</v-icon>
        Add Record
      </v-btn>
      <v-spacer></v-spacer>
      <v-text-field
        v-model="searchText"
        append-icon="mdi-magnify"
        label="Search"
        single-line
        hide-details
       />
       <v-btn class="ml-2" icon>
         <v-icon>mdi-dots-vertical</v-icon>
       </v-btn>
    </v-card-title>
    <v-data-table
    :headers="headers"
    :items="data"
    :search="searchText"
    :items-per-page="20"
    :loading="loader"
  >

  </v-data-table>
  </v-card>

</template>

<script>
export default {
  data: () => ({
    headers: [
      {
        text: 'name',
        value: 'name',
        align: 'start',
      },
      {
        text: 'Artist',
        value: 'artist',
      },
      {
        text: 'Genre',
        value: 'genre',
      },
    ],
    data: [
      {
        _id: '1',
        name: 'Wellness',
        artist: 'Last Dinosuars',
        genre: [
          'indie',
          'rock',
          'pop',
          'disco',
        ],
      },
    ],
    searchText: '',
    loader: false,
  }),
  methods: {

  },
};
</script>

<style>

</style>
