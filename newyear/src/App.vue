<template>
  <div class="app">
    <h1>{{ greeting }}</h1>
    <input v-model="name" type="text" placeholder="Введите ваше имя" />
    <button @click="showGreeting">Показать приветствие</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      greeting: '',
      name: ''
    }
  },
  methods: {
    showGreeting() {
      this.greeting = `С Новым годом, ${this.name}!`
    }
  }
}
</script>

<style>
.app {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-color: rgb(122, 255, 122);
  color: #FFF;
  font-family: 'Arial', sans-serif;
  font-size: 24px;
}

h1 {
  margin-bottom: 20px;
}

input {
  padding: 10px;
  margin-bottom: 10px;
  border-radius: 5px;
  border: none;
  outline: none;
}

button {
  padding: 10px 20px;
  font-size: 20px;
  color: #FFF;
  background-color: #C00;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #F00;
}
</style>
