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
                  <img class="icon" src="src/imagens/nachos.png" />
                </span>
              </div>

              <q-card-section>
                <div class="text-h6">Kits Salados</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                {{ lorem }}
              </q-card-section>
            </q-card>
          </q-intersection>
        </q-intersection>

        <q-intersection
          transition="fade"
          transition-duration="2000"
          class="example-item"
        >
          <q-intersection
            transition="slide-up"
            transition-duration="1000"
            class="example-item"
          >
            <q-card class="card-pedidos" flat bordered>
              <q-img src="src\imagens\salgados.jpg" />

              <q-card-section>
                <q-btn
                  fab
                  color="primary"
                  icon="place"
                  class="absolute"
                  style="top: 0; right: 12px; transform: translateY(-50%)"
                />

                <div class="row no-wrap items-center">
                  <div class="col text-h6 ellipsis">Individual</div>
                  <div
                    class="col-auto text-grey text-caption q-pt-md row no-wrap items-center"
                  >
                    <q-icon name="place" />
                    250 ft
                  </div>
                </div>

                <q-rating v-model="stars" :max="5" size="32px" />
              </q-card-section>

              <q-card-section class="q-pt-none">
                <div class="text-subtitle1">$・30 Salgados</div>
                <div class="text-caption text-grey">
                  Kit individual com 30 salgados com escola de 3 sabores de 10
                  em 10 sabores
                </div>
              </q-card-section>

              <q-separator />

              <q-card-actions>
                <q-btn flat round icon="event" />
                <q-btn flat color="primary"> Reserve </q-btn>
              </q-card-actions>
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
.h2-categoria {
  font-family: 'Montserrat', sans-serif;
  color: #000929;
  margin-left: 1rem;
  margin-top: 3rem;
  margin-bottom: 3rem;
  font-size: 32px;
}
.card-categoria {
  width: 23rem;
  height: 122px;
  background: #eeeeee;
  padding: 20px 0px 20px 20px;
  margin-top: 3rem;
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

.container-h2 {
  margin-top: 3rem;
  border-style: solid;
  border-width: 3px 0px 3px 0px;
  border-color: #dc9457;
}

.card-pedidos {
  margin-top: 10rem;
  border-radius: 1rem;
}
</style>
