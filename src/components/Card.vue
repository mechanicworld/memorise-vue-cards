<template>
  <v-card class="mx-auto" max-width="344">
    <v-card-text>
      <p class="tex text--primary">
        {{ card.word }}
      </p>

      <div class="text--primary">
        {{ card.example }}
        <v-form>
          <v-text-field
            v-model="guess"
            label="Guess"
            append-icon="mdi-help"
          />
        </v-form>
      </div>
    </v-card-text>
    <v-card-actions>
      <v-btn   text color="teal accent-4" @click="reveal = true">
        See the meaning
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <v-card
        v-if="reveal"
        class="transition-fast-in-fast-out v-card--reveal"
        :class="{ 'green': guess === card.meaning,'red': guess !== card.meaning }"
        style="height: 100%"
      >
        <v-card-text class="pb-0">
          <p class="display-1 text--primary">Meaning</p>
          <p>{{ card.meaning }}</p>
          <p> {{guess}} </p>
        </v-card-text>
        <v-card-actions class="pt-0">
          <v-btn text color="teal accent-4" @click="reveal = false">
            Close
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-expand-transition>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    reveal: false,
    guess:"",
    
  }),

  methods: {},
  props: {
    card: Object,
  },
};
</script>

<style scoped>
.v-card--reveal {
  bottom: 0;
  opacity: 1 !important;
  position: absolute;
  width: 100%;
}

.green{
  background: rgb(33, 169, 33);
}

.red{

  background-color: rgb(191, 61, 61);
}
</style>