<template>
  <h1>Essa é descrição de: {{ name }}</h1>
  <Info />
</template>

<script>

import Info from './Info.vue'

export default {
  name: "Pessoa",
  components:{
      Info
  },
  data() {
    return {
        name: 'Alexandre',
    };
  },
};
</script>
