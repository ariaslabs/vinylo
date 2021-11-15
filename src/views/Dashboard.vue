<template>
  <v-container fluid>
    <v-row>
      <v-col>
        <v-card class="mb-3">

        </v-card>
        <v-card flat>
          <v-card-title>
            <v-btn depressed>
              <v-icon left>
                mdi-plus
              </v-icon>
              Record</v-btn>
            <v-spacer></v-spacer>
            <v-text-field
              v-model="search"
              append-icon="mdi-magnify"
              label="Search"
              single-line
              hide-details
            ></v-text-field>
          </v-card-title>
          <v-data-table
          :headers="headers"
          :items="records"
          >
          </v-data-table>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "ID",
          value: "_id"
        },
        {

        },
        {
          text: "Name",
          align: 'start',
          value: "name"
        },
        {
          text: "Artist",
          align: 'start',
          value: "artist"
        },
        {
          text: "Album Length",
          value: "length"
        }
      ],
      records: [
        {
          _id: "3",
          name: "Wellness",
          artist: "Last Dinosaurs",
          length: "36:42",
          tracks: [
            {
              track: 1,
              volume: "a",
              name: ""
            }
          ],
          genres: [
            "Rock",
            "Alternitive",
            "Indie"
          ],

        }
      ]
    }
  },
  methods: {

  }
}
</script>

<style>

</style>