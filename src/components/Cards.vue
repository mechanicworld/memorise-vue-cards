<template>
  <div>
    <v-container>
      <v-row>
        <v-col cols="4" v-for="card in test" :key="card.id">
          <Card :card="card"/>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Card from "./Card";
export default {
  name: "Cards",
  data() {
    return {
      test: [
        {
          example: "Example sentences ",
          word: "Word 1",
          meaning: "Meaning 1",
          id: 1,
        },
        {
          example: "Example sentences ",
          word: "Word 2",
          meaning: "Meaning 2",
          id: 2,
        },
        {
          example: "Example sentences ",
          word: "Word 3",
          meaning: "Meaning 3",
          id: 3,
        },
        {
          example: "Example sentences ",
          word: "Word 4",
          meaning: "Meaning 4",
          id: 4,
        },
        {
          example: "Example sentences ",
          word: "Word 5",
          meaning: "Meaning 5",
          id: 5,
        },
        {
          example: "Example sentences ",
          word: "Word 6",
          meaning: "Meaning 6",
          id: 6,
        },
        
      ],
    };
  },
  components: {
    Card,
  },
};
</script>

<style>
</style>