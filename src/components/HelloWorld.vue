<template>
  <h1>{{ msg }}</h1>

<!-- My custom code -->
<div class="blocks">
  <button id="topbutton" class="button">add new</button>
  <button id="title" class="button">change new title</button>
  <button id="bg" class="button">change bg color</button>
  <button id="delete" class="button">delete last</button>
  
</div>
<div id="card" class="card">
  <h3 id="heading" class="heading">Landscaping Buisness!</h3>
  <img class="img" src="https://upload.wikimedia.org/wikipedia/commons/e/eb/Ash_Tree_-_geograph.org.uk_-_590710.jpg">
  <p>This is a green tree! We love trees and want to cut them for you :) </p>
  <button id="details" class="buttons">details</button>
</div>

  <button type="button" @click="state.count++">count is: {{ state.count }}</button>
  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  msg: String
})

const state = reactive({ count: 0 })
</script>

<script>

export default {
  methods: {
   const btn_title = document.getElementById("title");
const btn_bg = document.getElementById("bg");
const btn_details = document.getElementById("details");

document.querySelector("#topbutton").addEventListener('click', function(e) {
  const itemToClone = document.querySelector('.card').cloneNode(true);
  document.body.appendChild(itemToClone);
});

document.querySelector("#bg").addEventListener("click", function (e) {
  const card = document.getElementById("card");
  card.style.backgroundColor = "#9AE9EC";
});

btn_details.addEventListener("click", (e) => {
  let desc = btn_details.previousElementSibling;
  desc.style.display == "none"
    ? (desc.style.display = "")
    : (desc.style.display = "none");
});


document.querySelector("#title").addEventListener('click', function(e) {
  let name = prompt("Name Business....");
  if (name) {
    document.querySelector('.card h3').innerText = name;
  }
});

document.querySelector('#delete').addEventListener('click', function(e) {
  let wantsTo = confirm("Are you sure?");
  if (wantsTo) {
    if (document.querySelector('.card:last-child') !== document.querySelector('.card')) {
      document.querySelector('.card:last-child').remove();      
    }
    else {
      alert("YOU CAN NOT DELETE DREW!!!!");
    }
  }
});
  }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
