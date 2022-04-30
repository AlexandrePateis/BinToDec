<template>
  <div class="divisao">
    <Instructions />
    <Conversor />
    <History />
  </div>
    <footer class="footer">
      <Footer />
    </footer>
</template>

<script>

import Conversor from './components/Conversor.vue'
import Instructions from './components/Instructions.vue'
import History from './components/History.vue'
import Footer from './components/Footer.vue'

export default {
  name: "App",
  components: {
   Conversor,
   Instructions,
   History,
   Footer
  },
};
</script>
<style>
body{
  background-color: rgb(0, 0, 0);
}
.divisao{
  margin-top: 2em;
  display: flex;
  justify-content:space-between;
  width: 100%;
  gap: 10em;
}

</style>
