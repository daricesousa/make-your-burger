<script setup>

</script>


<template>
  <div>
    <p>Componente de mensagem</p>

    <form id="burger-form">
      <div class="input-container">
        <label for="name">Nome do cliente: </label>
        <input type="text" id="name" placeholder="Digite seu nome" />
      </div>
      <div class="input-container">
        <label for="bread">Escolha o pão: </label>
        <select name="bread" id="bread">
          <option value=""> Selecione o seu pão</option>
        </select>
      </div>
      <div class="input-container">
        <label for="meat">Escolha a carne do seu Burger: </label>
        <select name="meat" id="meat">
          <option value=""> Selecione o tipo de carne</option>
        </select>
      </div>
      <div id="option-container" class="input-container">
        <label id="option-title" for="option">Selecione os opcionais: </label>
        <div class="checkbox-container">
          <input type="checkbox" name="option" value="salame">
          <span> Salame</span>
        </div>
        <div class="checkbox-container">
          <input type="checkbox" name="option" value="salame">
          <span> Salame</span>
        </div>
        <div class="checkbox-container">
          <input type="checkbox" name="option" value="salame">
          <span> Salame</span>
        </div>
        <div class="checkbox-container">
          <input type="checkbox" name="option" value="salame">
          <span> Salame</span>
        </div>
        <div class="input-container">
          <input type="submit" class="submit-btn" value="Criar meu burger!">
        </div>
      </div>
    </form>


  </div>
</template>

<style scoped>
#burger-form {
  max-width: 400px;
  margin: 0 auto;
}

.input-container {
  display: flex;
  flex-direction: column;
  margin-bottom: 20px;
}

label {
  font-weight: bold;
  margin-bottom: 15px;
  color: #222;
  padding: 5px 10px;
  border-left: 4px solid #FCBA03;
}

input,
select {
  padding: 5px 10px;
  width: 300px
}

#option-container {
  flex-wrap: wrap;
  flex-direction: row;
}

#option-title {
  width: 100%;
}

.checkbox-container {
  display: flex;
  align-items: center;
  width: 50%;
  margin-bottom: 20px;
}

.checkbox-container span,
.checkbox-container input {
  width: auto;
}

.checkbox-container span {
  margin-left: 6px;
  font-weight: bold;
  ;
}

.submit-btn {
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

.submit-btn:hover {
  background-color: transparent;
}
</style>
