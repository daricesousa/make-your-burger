<script setup>

import { onMounted, ref } from 'vue';

const orders = ref([]);

async function getOrders() {
  const req = await fetch("http://localhost:3000/burgers");
  const data = await req.json();
  orders.value = data;
}

onMounted(() => getOrders());


</script>

<template>
  <div id="burger-table">
    <div>
      <div id="burger-table-heading" class="burger-table-row">
        <div class="order-id">#:</div>
        <div>Cliente</div>
        <div>Pão</div>
        <div>Carne</div>
        <div>Opcionais</div>
        <div>Ações</div>
      </div>
      <div id="burger-table-rows" v-for="order in orders" :key="order.id">
        <div class="burger-table-row">
          <div class="order-number">{{ order.id }}</div>
          <div>{{ order.name }}</div>
          <div> {{ order.bread }}</div>
          <div>{{ order.meat }}</div>
          <div>
            <ul v-for="(optional, index) in order.optional" :key="index">
              <li>{{ optional }}</li>
            </ul>
          </div>
          <select name="status" class="status">
            <option value="">{{ order.status }}</option>
          </select>
          <button class="delete-btn">Cancelar</button>
        </div>
      </div>
    </div>

  </div>
</template>


<style scoped>
#burger-table {
  max-width: 1200px;
  margin: 0 auto;
}

.burger-table-row div,
#burger-table-heading div {
  width: 16%;
}

#burger-table-heading {
  /* font-weight: bold; */
  color: #FCBA03;
  padding: 12px;
  border-bottom: 3px solid #333;
}

.burger-table-row {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  padding: 12px;
  border: 1px solid #CCC;
}

#burger-table-heading .order-id,
.burger-table-row .order-number {
  width: 5%;
}

select {
  padding: 12px 6px;
  margin-right: 12px;
}

.delete-btn {
  background-color: #222;
  color: #FCBA03;
  font-weight: bold;
  border: 2px solid #222;
  padding: 10px;
  font-size: 16px;
  /* margin: 0 auto; */
  cursor: pointer;
  transition: .5s;
}

.delete-btn:hover {
  background-color: transparent;
}
</style>