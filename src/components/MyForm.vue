<template>
  <div>
    <form @submit.prevent="onCreatePost">
      <label for="cardNumber">Номер карты</label>
      <input type="text" id="cardNumber" v-model="cardNumber">
      <br>
      <label for="cardDate">Действует до</label>
      <input type="text" id="cardDate" v-model="cardDate">
      <br>
      <label for="cardholder">Имя держателя карты</label>
      <input type="text" id="cardholder" v-model="cardholder">
      <br>
      <label for="cardCvv">CVV</label>
      <input type="text" id="cardCvv" v-model="cardCvv">
      <br>
      <label for="submit">Отправить</label>
      <input type="submit" id="submit">
    </form>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  data() {
    return {
      cardNumber: '',
      cardDate: '',
      cardholder: '',
      cardCvv: '',
    }
  },
  methods: {
    onCreatePost() {
      axios.post(
          'здесь_должен_быть_сервер',
          {
            cardNumber: this.cardNumber,
            cardDate: this.cardDate,
            cardholder: this.cardholder,
            cardCvv: this.cardCvv,
          }).then(response => {
            console.log(response)
      })
    }
  },
  name: 'MyForm',
  props: {

  }
}
</script>

<style scoped>

</style>
