<template>
  <v-form>
    <v-select placeholder="Choose option" class="rounded" v-model="option" :items="options" filled/>
    <v-select placeholder="Choose currency" class="rounded" v-model="currency" :items="currencies"  item-text="" filled/>
    <v-img class="qr-img" src="../assets/qr.png" />
    <p class="code">Some code there</p>
    <v-btn class="primary v-picker--full-width">Copy</v-btn>
  </v-form>
</template>

<script>
export default {
  data: function () {
    return {
      option: "",
      currency: "",
      options: ["Kraken", "Something else"],
      currencies: ["USD", "RUB", "USDT"],
    }
  }
}
</script>

<style scoped>
.qr-img {
  display: block;
  max-width: 120px;
  margin-top: 10px;
  margin-left: auto;
  margin-right: auto;
}

.code {
  text-align: center;
  margin-top: 27px;
  margin-bottom: 27px;
}
</style>
