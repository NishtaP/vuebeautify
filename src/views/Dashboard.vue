<template>
  <div>
    <h1>Dashboard</h1>
    <v-data-table
      :headers="headers"
      :items="desserts"
      :items-per-page="5"
      class="elevation-1"
      @click:row="selectRow"
    ></v-data-table>
    <v-snackbar v-model="snackbar">
      You have selected {{ currentItem }}
      <v-btn color="pink" text @click="snackbar = false">Close</v-btn>
    </v-snackbar>
  </div>
</template>

<script>
export default {
  name: "DashboardPage",
  data() {
    return {
      currentItem: "",
      snackbar: false,
      headers: [
        // Data hidden for brevity
      ],
      desserts: [
        // Data hidden for brevity
      ]
    };
  },
  methods: {
    selectRow(event) {
      this.snackbar = true;
      this.currentItem = event.name;
    }
  }
};
</script>