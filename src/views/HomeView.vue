<script>
import ButtonComponent from '../components/ButtonComponent.vue';

export default {
  components: {
    ButtonComponent,
  }, 

  data() {
        return {}
    },
}
</script>

<template>
  <div class="container">
    <div class="contain">
      (HOVER)
      <button-component>
      </button-component>
    </div>
  </div>
</template>

<style>
.container {
  margin: 0 auto;
  max-width: 1548px;
}

.contain {
  margin-top: 50px;
  padding: 72px 95px;
  border: 8px solid var(--white);
}
</style>

