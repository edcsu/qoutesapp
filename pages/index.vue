<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <Qoutecard class="my-8" :qoute="qoute" :loading="loading" @generate="getQoute"/>
    </v-col>
  </v-row>
</template>

<script>
import Qoutecard from "~/components/qoutecard.vue";
export default {
    name: "IndexPage",
    components: { Qoutecard },
    async asyncData ({ $config: { baseApiUrl }, $axios}) {
    try {
      let { data } = await $axios.get(`${baseApiUrl}/random`);
      return { qoute: data };
     } catch (error) {
        console.error(error);
     }
    },
    data: () => ({
        loading: false,
        qoute: {}
    }),
    methods: {
      async getQoute(){
        try {
          this.loading = true;
          let { data } = await this.$axios.get(`${this.$config.baseApiUrl}/random`);
          this.loading = false;
          this.qoute = data;
        } catch (error) {
          this.loading = false;
          console.error(error);
        }
      }
    }
}

</script>
