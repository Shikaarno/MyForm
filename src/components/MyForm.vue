<template>
  <div>
    <form action="">
      <label for="cardNumber">Номер карты</label>
      <input type="text" id="cardNumber">
      <br>
      <label for="cardDate">Действует до</label>
      <input type="text" id="cardDate">
      <br>
      <label for="cardholderName">Имя держателя карты</label>
      <input type="text" id="cardholderName">
      <br>
      <label for="cardCvv">CVV</label>
      <input type="text" id="cardCvv">
    </form>
  </div>
</template>

<script>
export default {
  name: 'MyForm',
  props: {

  }
}
</script>

<style scoped>

</style>
