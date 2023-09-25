<script setup>

const props = defineProps(["msg"]);

</script>

<template>
  <div class="message-container">
    <p> {{ props.msg }}</p>
  </div>
</template>


<style scoped>
.message-container {
  color: #004085;
  background-color: #CCE5FF;
  border: 2px solid #B8DAFF;
  border-radius: 5px;
  padding: 10px;
  max-width: 400px;
  margin: 30px auto;

}
</style>