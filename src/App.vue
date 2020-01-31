<template>
  <div id="app">
    <Header />
    <Boodschappen v-bind:Boodschappen="Boodschappen" v-on:del-Boodschap="deleteBoodschap" />
    <BoodschapToevoegen v-on:add-Boodschap="BoodschapToevoegen" />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/layout/header";
import Boodschappen from "./components/Boodschappen";
import BoodschapToevoegen from "./components/BoodschapToevoegen";
import Footer from "./components/layout/footer";

export default {
  name: "app",
  components: {
    Header,
    Boodschappen,
    BoodschapToevoegen,
    Footer
  },
  data() {
    return {
      Boodschappen: [
        {
          id: 1,
          title: "Komkommer",
          completed: false
        },
        {
          id: 2,
          title: "Melk",
          completed: false
        },
        {
          id: 3,
          title: "Boter",
          completed: false
        },
        {
          id: 4,
          title: "Koekjes",
          completed: false
        },
        {
          id: 5,
          title: "Cola",
          completed: false
        },
        {
          id: 6,
          title: "Limonade",
          completed: false
        }
      ]
    };
  },
  methods: {
    deleteBoodschap(id) {
      this.Boodschappen = this.Boodschappen.filter(Boodschap => Boodschap.id !== id);
    },
    BoodschapToevoegen(newBoodschap) {
      this.Boodschappen = [...this.Boodschappen, newBoodschap];
    }
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}

.btn {
  display: inline-block;
  background-color: #fff;
  border: none;
  color: #000;
  padding: 12px 25px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  transition: .3s;
  margin-top: 15px;
  margin-left: 10px;
  border-radius: 20px;
  border: 1px solid #000;
}

.btn:hover {
  transform: scale(1.1);
}
</style>
