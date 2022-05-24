<template>
  <div v-show="isVisible" class="modal-back">
    <v-card light class="modal">
      <v-tabs v-model="tab">
        <v-tabs-slider></v-tabs-slider>

        <v-tab :key="1">
          Deposit
        </v-tab>
        <v-tab :key="2">
          Withdraw
        </v-tab>
        <v-tab :key="3">
          Rebalance
        </v-tab>

        <v-divider/>
        <v-btn icon @click="closeModal">
          <v-icon>mdi-close</v-icon>
        </v-btn>
      </v-tabs>

      <v-tabs-items v-model="tab" class="pt-5">
        <v-tab-item :key="1">
          <Deposit/>
        </v-tab-item>
        <v-tab-item :key="2">
          <Withdraw/>
        </v-tab-item>
        <v-tab-item :key="3">
          <Rebalance/>
        </v-tab-item>
      </v-tabs-items>
    </v-card>
  </div>
</template>
<script>
import Deposit from "@/components/Deposit";
import Withdraw from "@/components/Withdraw";
import Rebalance from "@/components/Rebalance";

export default {
  data: function () {
    return {
      tab: null,
      //can be easily changed to false to be used as actual modal
      isVisible: true,
    }
  },
  methods: {
    closeModal: function () {
    }
  },
  components: {Rebalance, Withdraw, Deposit}
}
</script>

<style scoped>
.modal-back {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.6);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal {
  width: 400px;
  z-index: 2;
  padding: 10px;
}
</style>
