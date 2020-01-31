<template>
  <header class="header">
    <h1>Jouw boodschappenlijstje</h1>
    <p>Voeg hier boodschappen toe die je niet moet vergeten in de supermarkt.</p>
  </header>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
.header {
  background: #0074ff;
  color: #fff;
  text-align: center;
  padding: 10px;
  border-bottom: 2px solid #000;
}

.header a {
  color: #fff;
  padding-right: 5px;
}
</style>