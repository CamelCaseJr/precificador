<template>
  <q-layout view="lHh lpR fFf">
    <HeaderComponent @atualizarDrawer="atualizar" />

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from 'vue';
import HeaderComponent from '../components/HeaderComponent.vue';
export default {
  data() {
    return {
      isAberto: ref(false),
    };
  },

  components: {
    HeaderComponent,
  },
  methods: {
    atualizar() {
      this.isAberto = !this.isAberto;
    },
  },
};
</script>

<style></style>
