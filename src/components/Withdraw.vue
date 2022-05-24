<template>
  <v-form>
    <v-select placeholder="Choose exchange" class="rounded" :items="[]" filled/>
    <v-select placeholder="Choose currency" class="rounded" :items="[]" filled/>
    <v-text-field class="rounded" label="Withdraw amount" filled/>
    <v-btn class="primary v-picker--full-width">Withdraw</v-btn>
  </v-form>
</template>
