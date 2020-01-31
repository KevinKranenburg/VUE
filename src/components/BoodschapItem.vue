<template>
  <div class="Boodschap-item" v-bind:class="{'is-complete':Boodschap.completed}">
    <p>
      <input class="check-custom" type="checkbox" v-on:change="markComplete" />
      {{ Boodschap.title }}
      <button @click="$emit('del-Boodschap', Boodschap.id)" class="del">x</button>
    </p>
  </div>
</template>

<script>
export default {
  name: "BoodschapItem",
  props: ["Boodschap"],
  methods: {
    markComplete() {
      this.Boodschap.completed = !this.Boodschap.completed;
    }
  }
};
</script>

<style scoped>
.Boodschap-item {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px #000 solid;
}

.is-complete {
  text-decoration: line-through;
}

.del {
  background: #ff0000;
  color: #fff;
  padding: 5px 9px;
  border-radius: 50%;
  cursor: pointer;
  float: right;
}

input {
    height: 30px;
    width: 30px;
}
</style>