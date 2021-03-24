<template>
  <Header :title="title" />
  <Account />
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Header from "./components/Header";
import Account from "./components/Account";

export default {
  name: 'App',
  components: {
    Header,
    HelloWorld,
    Account,
  },
  data() {
    return {
      title: "Título de mi app",
      msg: "Hola Mundo"
    };
  }
}
</script>

<style>
:root {
  --green: #3ba776;
  --blue: #5e9aed;
  --orange: #ee822b;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  min-height: 100vh;
  background-color: #222;
  display: flex;
  justify-content: center;
  align-items: center;
}

#app {
  font-family: Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #fff;
}

.text-left {
  text-align: left;
}

.text-center {
  text-align: center;
}

.text-right {
  text-align: right;
}

.mb-2 {
  margin-bottom: 20px;
}

.ml-2 {
  margin-left: 20px;
}

.ml-3 {
  margin-left: 30px;
}

.ml-4 {
  margin-left: 40px;
}

.mb-4 {
  margin-bottom: 40px;
}

.green {
  color: var(--green);
}

.blue {
  color: var(--blue);
}

.orange {
  color: var(--orange);
}

.btn {
  padding: 10px 15px;
  font-size: 1.1rem;
  color: #222;
  background-color: #eee;
  border-radius: 5px;
  font-weight: bold;
  border: none;
  outline: none;
  cursor: pointer;
  min-width: 50px;
}

.btn:disabled,
.btn:disabled:hover {
  cursor: auto;
  color: #ccc;
  background-color: #eee;
}

.btn-primary {
  background-color: var(--blue);
  color: #fff;
  transition: 400ms ease-in-out;
}

.btn-primary:hover {
  background-color: var(--orange);
  color: #222;
}
</style>
