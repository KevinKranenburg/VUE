<template>
  <footer class="footer">
    <h3>
      Copyright 2020
      <a href="http://www.kevinkranenburg.nl/" target="_blank">www.kevinkranenburg.nl</a>
    </h3>
  </footer>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style scoped>
.footer {
  background: #0074ff;
  color: #fff;
  text-align: center;
  border-top: 2px solid #000;
  padding: 10px;
  bottom: 0;
  text-align: center;
  position: absolute;
  width: 100%;
}

.footer a {
  color: #fff;
  padding-right: 5px;
  text-decoration: none;
}
</style>