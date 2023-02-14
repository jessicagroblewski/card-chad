<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3 + Vite" />
</template>

<script setup>
import HelloWorld from './components/HelloWorld.vue'

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.card {
  background-color: #91EBA9;
  border: 5px outset #217C07;
  width: 400px;
  height: 500px;
  text-align:center;
}
.heading{
  color: white;
  -webkit-text-stroke: 1px #1D6508;
  font-size: 26px;
}
button {
  text-transform: uppercase;
  color: blue;
  padding: 16px 16px;
  background-color: pink;
  padding: 15px 15px 15px 15px; //top right bottom left
  }

img {
  width: 200px;
}
.ptag {
  font-size: 20px;
}
.btn {
  visibility: hidden;
  border: 8px dashed blue;
  margin: 12px 12px;
}
button:hover {
  text-transform: uppercase;
  color: black;
  padding: 16px 16px;
  background-color: white;
}

button:focus {
  outline: 4px dashed darkorange;
}

@media only screen and (min-width: 500px) and (max-width: 800px) {
  .btn {
    visibility: visible;
    border: 8px dashed blue;
    margin: 12px 12px;
  }
}
@media screen and (max-device-width: 500px) {
  body {
    transform: scale(500px);
  }
}
.card p{
  margin: 10px;
}

.buttons{
  display: block;
 }


input:checked + label + .description { display:none; }



</style>
