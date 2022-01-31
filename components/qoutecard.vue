<template>
  <v-card :loading="loading">
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
            v-for="tag in tags"
            :key="tag"
          >
            {{ tag }}
          </v-chip>
        </v-chip-group>
      </v-card-text>
        <v-card-title class="headline">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
          Sint quas aliquam delectus repellendus incidunt dolorum aperiam odio voluptatum nihil! 
          Quasi consequatur dolore necessitatibus nihil inventore debitis dicta porro ipsum quod.
        </v-card-title>
        <v-card-subtitle>John doe</v-card-subtitle>
        <v-card-actions>
          <v-spacer />
          <v-btn color="primary"> Generate </v-btn>
        </v-card-actions>
      </v-card>
</template>

<script>
export default {
    data: () => ({
        loading: false,
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
}
</script>

<style>

</style>