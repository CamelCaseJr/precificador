<template>
  <q-intersection
    transition="fade"
    transition-duration="3000"
    class="example-item"
  >
    >
    <q-card class="card-pedidos" flat bordered>
      <q-img src="imagens\salgados.jpg" />

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
          Kit individual com 30 salgados com escola de 3 sabores de 10 em 10
          sabores
        </div>
      </q-card-section>

      <q-separator />

      <div class="container-bt-cart">
        <q-btn
          flat
          class="q-gutter-sm"
          style="width: 100ch; border-radius: 1rem"
        >
          <q-avatar size="42px">
            <img src="icons\carrinho-de-compras.png" />
          </q-avatar>
          Adicionar
        </q-btn>
      </div>
    </q-card>
  </q-intersection>
</template>

<script>
export default {};
</script>

<style>
.card-pedidos {
  margin-top: 10rem;
  margin-bottom: 3rem;
  border-radius: 1rem;
}

.container-bt-cart {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
