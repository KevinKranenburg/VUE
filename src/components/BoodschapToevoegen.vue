<template>
  <div class="toevoegen">
    <form @submit="BoodschapToevoegen">
      <input
        class="invoer-veld"
        type="text"
        v-model="title"
        name="title"
        placeholder="Nieuwe boodschap..."
      />
      <input type="submit" value="submit" class="btn" />
    </form>
  </div>
</template>

<script>
export default {
  name: "BoodschapToevoegen",
  data() {
    return {
      title: ""
    };
  },
  methods: {
    BoodschapToevoegen(e) {
      e.preventDefault();
      const newBoodschap = {
        title: this.title,
        completed: false
      };
      this.$emit("add-Boodschap", newBoodschap);
      this.title = "";
    }
  }
};
</script>

<style scoped>
form {
  display: flex;
  position: relative;
  display: block;
}

input [type="text"] {
  flex: 10;
  padding: 5px;
  text-align: center;
}

input [type="submit"] {
  flex: 2;
}

.toevoegen {
  background: #0074ff;
  width: 100%;
  text-align: center;
  height: 80px;
  border-bottom: 2px solid #000;
}

.invoer-veld {
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #000;
  border-radius: 4px;
  box-sizing: border-box;
  width: 300px;
  text-align: center;
  font-size: 16px;
  color: #000;
}
</style>