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
      <h2>olá</h2>
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
  padding-top: 2rem;
  padding-left: 0.5rem;
  display: flex;
  align-items: center;
}

p {
  color: #fafafa;
  margin: 0; // Remove as margens padrão
  font-family: 'Montserrat', sans-serif;
  font-size: 36px;
}
.destacado {
  background: linear-gradient(to right, #ff0000, #ff6666, #ffcdd2);
  -webkit-background-clip: text; /* Para navegadores baseados em WebKit, como Chrome e Safari */
  background-clip: text;
  color: transparent; /* Torna o texto transparente */
  font-size: 42px;
}
</style>
