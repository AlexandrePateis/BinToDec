<template>
  <div class="divisao">
    <Instructions />
    <Conversor />
    <History />
  </div>
    
</template>

<script>

import Conversor from './components/Conversor.vue'
import Instructions from './components/Instructions.vue'
import History from './components/History.vue'

export default {
  name: "App",
  components: {
   Conversor,
   Instructions,
   History
  },
};
</script>
<style>
body{
  background-color: rgb(0, 0, 0);
}
.divisao{
  display: flex;
  justify-content:space-between;
  width: 100%;
  
}
</style>
