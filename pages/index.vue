<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <Qoutecard />
    </v-col>
  </v-row>
</template>

<script>
import Qoutecard from "~/components/qoutecard.vue";
export default {
    name: "IndexPage",
    components: { Qoutecard }
}
</script>
