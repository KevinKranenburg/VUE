<template>
  <div>
    <div v-bind:key="Boodschap.id" v-for="Boodschap in Boodschappen">
      <BoodschapItem v-bind:Boodschap="Boodschap" v-on:del-Boodschap="$emit('del-Boodschap', Boodschap.id)" />
    </div>
  </div>
</template>

<script>
import BoodschapItem from "./BoodschapItem.vue";
export default {
  name: "Boodschappen",
  components: {
    BoodschapItem
  },
  props: ["Boodschappen"]
};
</script>

<style scoped>
</style>