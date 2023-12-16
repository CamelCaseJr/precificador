<template>
  <div>
    <q-page class="container-page">
      <q-card flat class="my-card">
        <q-card-section>
          <div class="text-card">Descubra Novos Sabores!</div>
        </q-card-section>
      </q-card>
    </q-page>
    <q-page>
      <div class="container-categories">
        <div class="container-h2">
          <h2 class="h2-categoria elementor-size-default">Categorias</h2>
        </div>
        <CardCategoriasComponent />

        <CardItensComponent />
      </div>
    </q-page>
  </div>
</template>

<script>
import CardItensComponent from '../components/CardItensComponent.vue';
import CardCategoriasComponent from '../components/CardCategoriasComponent.vue';
import coxinhaCapa from '../imagens/coxinha-capa.jpg';
import coxinhaImage from '../imagens/coxinha.jpg';
import { ref } from 'vue';
export default {
  data() {
    return {
      images: [coxinhaCapa, coxinhaImage],
      slide: ref(1),
      autoplay: ref(true),
    };
  },
  components: {
    CardItensComponent,
    CardCategoriasComponent,
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Yanone+Kaffeesatz:wght@700&display=swap');
.container-page {
  padding-top: 5rem;
}

.my-card {
  background-image: url('../imagens/coxinha-capa.jpg');
  background-size: cover;
  background-position: center;
  align-items: center;
  text-align: center;
  padding-top: 1rem;
}

.text-card {
  font-family: 'Yanone Kaffeesatz', sans-serif;
  font-size: 72px;
  opacity: 1;
  padding-top: 10rem;
  padding-bottom: 10rem;
  top: 100%;
  color: #fafafa;
}

.container-categories {
  padding: 0 15px;
}
.h2-categoria {
  font-family: 'Montserrat', sans-serif;
  color: #000929;
  margin-left: 1rem;
  margin-top: 3rem;
  margin-bottom: 3rem;
  font-size: 32px;
}

.container-h2 {
  margin-top: 3rem;
  border-style: solid;
  border-width: 3px 0px 3px 0px;
  border-color: #fc3939;
  display: flex;
  justify-content: center;
  align-items: center;
}
.card-itens-container {
  max-height: 400px;
}
</style>
