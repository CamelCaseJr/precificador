<template>
  <q-intersection
    transition="fade"
    transition-duration="3000"
    class="example-item"
  >
    <q-intersection
      transition="slide-right"
      transition-duration="2000"
      class="example-item"
    >
      <q-card class="card-categoria row no-shadow">
        <div class="categories-icon">
          <span>
            <img class="icon" :href="props.linkImg" />
          </span>
        </div>

        <q-card-section>
          <div class="text-h6">{{ props.nome }}</div>
        </q-card-section>
      </q-card>
    </q-intersection>
  </q-intersection>
</template>

<script setup>
const props = defineProps({
  nome: {
    type: String,
  },
  linkImg: {
    type: URL,
  },
});
</script>
<style>
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
</style>
