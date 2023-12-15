<template>
  <div>
    <q-page class="container-page">
      <div class="content">
        <P>
          A Melhor <br />Salgaderia <br />
          Do Bairro.
          <br />
        </P>
      </div>
    </q-page>
    <q-page>
      <div class="container-categories">
        <div class="container-h2">
          <h2 class="h2-categoria elementor-size-default">Categorias</h2>
        </div>
        <CardCategoriasComponent />
        <div class="card-itens-container">
          <q-intersection
            transition="fade"
            transition-duration="1000"
            class="example-item"
          >
            <q-intersection transition="slide-up" class="example-item">
              <CardItensComponent />
            </q-intersection>
          </q-intersection>
        </div>
      </div>
    </q-page>
  </div>
</template>

<script>
import CardItensComponent from '../components/CardItensComponent.vue';
import CardCategoriasComponent from '../components/CardCategoriasComponent.vue';
export default {
  components: {
    CardItensComponent,
    CardCategoriasComponent,
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700&display=swap');
.container-page {
  background-image: url('../imagens/coxinha.jpg');
  background-size: cover;
  background-position: center;
  height: 100vh; // Defina a altura para ocupar a tela inteira, se necessário
}
.content {
  align-items: center;
  text-align: center;
  padding-top: 1rem;
}

p {
  color: #fafafa;
  margin: 0; // Remove as margens padrão
  font-family: 'Montserrat', sans-serif;
  font-size: 48px;
  margin-left: 10px;
  text-align: left;
}
.destacado {
  background: linear-gradient(to right, #ff0000, #ff6666, #ffcdd2);
  -webkit-background-clip: text; /* Para navegadores baseados em WebKit, como Chrome e Safari */
  background-clip: text;
  color: transparent; /* Torna o texto transparente */
  font-size: 42px;
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
  border-color: #dc9457;
  display: flex;
  justify-content: center;
  align-items: center;
}
.card-itens-container {
  max-height: 400px;
}
</style>
