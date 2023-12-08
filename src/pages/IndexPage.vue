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
        <p class="p-categoria">Categorias</p>
        <q-intersection
          transition="fade"
          transition-duration="3000"
          class="example-item"
        >
          <q-intersection
            transition="slide-right"
            transition-duration="1000"
            class="example-item"
          >
            <q-card class="card-categoria row no-shadow">
              <div class="categories-icon">
                <span>
                  <img class="icon" src="src/imagens/individual.png" />
                </span>
              </div>

              <q-card-section>
                <div class="text-h6">Our Changing Planet</div>
                <div class="text-subtitle2">by John Doe</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                {{ lorem }}
              </q-card-section>
            </q-card>
          </q-intersection>
        </q-intersection>
      </div>
    </q-page>
  </div>
</template>

<script setup lang="ts"></script>

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
.p-categoria {
  font-family: 'Montserrat', sans-serif;
  color: #000929;
  margin-left: 1rem;
  margin-top: 3rem;
  margin-bottom: 3rem;
  font-size: 32px;
}
.card-categoria {
  width: 444px;
  height: 122px;
  background: #eeeeee;
  padding: 20px 0px 20px 20px;
  border-radius: 20px;
  text-align: center;
  position: relative;
  z-index: 1;
  transition: all 0.3s ease 0s;
  display: flex;
  align-items: center;
  gap: 12px;
}
.categories-icon {
  display: flex;
  justify-content: center;
}
.icon {
  width: 82px;
  height: 82px;
  text-align: center;
  line-height: 82px;
  transition: all 0.8s ease 0s;
}
</style>
