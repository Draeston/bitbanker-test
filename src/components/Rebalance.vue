<template>
  <v-form>
    <p>From</p>
    <v-select placeholder="Choose exchange" class="rounded" :items="[]" filled/>
    <p>To</p>
    <v-select placeholder="Choose exchange" class="rounded" :items="[]" filled/>
    <v-select placeholder="Choose currency" class="rounded" :items="[]" filled/>
    <v-text-field label="Transfer amount" class="rounded mb-0" filled />
    <v-card class="pa-3 mb-2 mt-0">
      <v-card class="primary white--text pa-2 mt-0">Balance: </v-card>
      <v-chip-group>
        <v-chip>10%</v-chip>
        <v-chip>25%</v-chip>
        <v-chip>50%</v-chip>
        <v-chip>100%</v-chip>
        <v-chip>Split</v-chip>
      </v-chip-group>
    </v-card>
    <v-btn class="primary v-picker--full-width">Apply</v-btn>
  </v-form>
</template>
