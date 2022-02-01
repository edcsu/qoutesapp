<template>
  <v-card :loading="loading" color="#26c6da">
    <template slot="progress">
        <v-progress-linear
            color="deep-purple"
            height="10"
            indeterminate
        ></v-progress-linear>
    </template>
  <v-card-text>
    <v-chip-group
      column
    >
      <v-chip
        v-for="tag in qoute.tags"
        :key="tag"
      >
        {{ tag }}
      </v-chip>
    </v-chip-group>
  </v-card-text>
    <v-card-title v-text="qoute.content" class="headline">
    </v-card-title>
    <v-card-subtitle v-text="qoute.author"></v-card-subtitle>
    <v-card-actions>
      <v-spacer />
      <v-btn color="primary mr-4 mb-2" x-large @click.prevent="emitEvent()"> Generate </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
    props: [ 'qoute', 'loading'],
    data: () => ({
        tags: [
            'Work',
            'Home Improvement',
            'Vacation',
            'Food',
            'Drawers',
            'Shopping',
            'Art',
            'Tech',
            'Creative Writing',
        ],
    }),
    methods: {
    emitEvent() {
      this.$emit("generate");
    }
  }
}
</script>

<style>

</style>