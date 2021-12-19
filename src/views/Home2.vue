<template>
  <v-card>
    <h1>Hello chello</h1>
    <v-btn @click="getData()" color="colorPrimary"> Hello </v-btn>
  </v-card>
</template>
<script lang="ts">
import { Vue, Component, Prop } from "vue-property-decorator";
import { VCard } from "vuetify/lib/components";
import DataService from "@/services/DataService";

@Component({
  components: {
    VCard,
  },
})
export default class Home2 extends Vue {
  private dataService: DataService = new DataService();

  constructor() {
    super();
  }

  private getData() {
    const message = this.dataService.getData("test");
    console.log(message);
  }
}
</script>
