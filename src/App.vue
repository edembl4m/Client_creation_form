<template>
  <div id="app">
    <div class="container">
      <h1 class="title-h1">Создание клиента</h1>
      <div class="form-wrapper">
        <CreateUserForm />
      </div>
    </div>
  </div>
</template>

<script>
import CreateUserForm from './components/CreateUserForm.vue';


export default {
  name: 'App',
  components: {
    CreateUserForm
}
}
</script>

<style lang="scss">
@import "@/styles/main.scss";
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // color: #2c3e50;
  color: #0b1f33;;
  background-color: #fafcff;
}

.container {
  max-width: 1366px;
  border: 1px solid black;
  margin: 0 auto;
}

.title-h1 {
  font-size: 32px;
  margin-top: 30px;
  margin-bottom: 30px;
}

.form-wrapper {
  background-color: white;
  max-width: 904px;
  padding: 24px;
  border-radius: 10px;
  -webkit-box-shadow: 4px 4px 8px -3px rgba(34, 60, 80, 0.2);
  -moz-box-shadow: 4px 4px 8px -3px rgba(34, 60, 80, 0.2);
  box-shadow: 4px 4px 8px -3px rgba(34, 60, 80, 0.2);
}
</style>
