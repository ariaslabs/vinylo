<template>
  <v-container fluid>
    <v-row>
      <v-col>
        <TableView />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import TableView from '../components/TableVIew.vue';

export default {
  name: 'Home',
  data: () => ({
    records: [
      {
        _id: '12481hi2h410',
        albuim: 'Wellness',
        artist: 'Last Dinosaurs',

      },
    ],
  }),
  components: {
    TableView,
  },
  methods: {
    addRecord() {

    },
    getRecords() {

    },
  },
};
</script>
