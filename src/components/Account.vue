<template>
  <section>
    <h2 class="green">Saldo: <span class="blue">{{ balance }}</span></h2>
    <h2 class="green">Tipo de cuenta: <span class="blue">{{ cuenta }}</span></h2>
    <h2 class="green">Estado: <span class="blue">{{ accountStatus }}</span></h2><br>
    <h2 class="orange mb-2">Servicios</h2>

    <ol class="ml-2 mb-2">
      <li v-for="(service, index) in services" :key="index">{{ service }}</li>
    </ol>

    <ModifyBalance
      text="+"
      @action="increase"
    />&nbsp;

    <ModifyBalance
      text="-"
      @action="decrease"
      v-bind:disable="disable"
    />
  </section>
</template>

<script>
import ModifyBalance from "./ModifyBalance";

export default {
  name: "Account",
  components: {
    ModifyBalance,
  },
  data() {
    return {
      balance: 100,
      cuenta: "Visa",
      status: true,
      services: ["Saldo", "Prestamos", "Inversiones"],
      disable: false
    }
  },
  methods: {
    increase() {
      this.disable = this.disable && false;
      this.balance = this.balance + 100;
    },
    decrease() {
      if (this.balance < 100) {
        this.disable = true;
      }

      if(this.balance !== 0) {
        this.balance = this.balance - 100;
      }
    }
  },
  computed: {
    accountStatus() {
      return this.status ? "Activa" : "Desactivada";
    }
  }
};
</script>

<style scoped>
</style>