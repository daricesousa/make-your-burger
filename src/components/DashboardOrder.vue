<script setup>
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
      <div id="burger-table-rows">
        <div class="burger-table-row">
          <div class="order-number">1</div>
          <div> João</div>
          <div> Integral</div>
          <div>Maminha</div>
          <div>
            <ul>
              <li> Salame</li>
              <li> Tomate</li>
            </ul>
          </div>
          <select name="status" class="status">
            <option value="">Fazendo</option>
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