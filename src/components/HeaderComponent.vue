<template>
  <q-header class="container-header">
    <q-toolbar>
      <q-btn dense flat round icon="home" @click="clickBt" />

      <q-toolbar-title class="container-toolbar"> +HuMm </q-toolbar-title>
      <q-btn dense flat round icon="menu" @click="clickBt" />
    </q-toolbar>
  </q-header>
</template>

<script>
import { ref } from 'vue';

export default {
  data() {
    return {
      dadoBooleano: ref(false),
    };
  },
  methods: {
    clickBt() {
      this.dadoBooleano = true;
      this.$emit('atualizarDrawer', this.dadoBooleano);
    },
  },
};
</script>
<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=PT+Sans+Narrow:wght@700&display=swap');
.container-header {
  background-color: #000929;
  color: #edebee;
  height: 5rem;

  // Centraliza o conteúdo verticalmente
  display: flex;
  align-items: center;
}
.container-toolbar {
  font-family: 'PT Sans Narrow', sans-serif;
}
</style>
