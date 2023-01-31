<template>
  <div class="error-block">
    <h3>Ой-ой! У нас ошибка, но все под контролем :)</h3>
    <h3>Статус: {{ error.statusCode }}</h3>
    <h3>Сообщение об ошибке: {{ error.message }}</h3>
  </div>
</template>

<script>

  export default {
    props: {
      error: {
        type: Object,
        default: () => ({})
      }
    },
    mounted() {
      console.log(this.error, 'ERROR OBJECT')
    }
  }
</script>

<style scoped>
  .error-block {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    height: 100vh;
  }
</style>
