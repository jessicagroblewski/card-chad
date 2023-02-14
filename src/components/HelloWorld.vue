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
    hoover() {
      document.querySelectorAll(".card").forEach((item) => {
        if(!item.classList.contains("hoverCard")){
          item.classList.add("hoverCard");
          console.log(item);
        }
        else{
          item.classList.remove("hoverCard");
          console.log(item);
        }
      });
    },
    
    duplicate() {
      const cloneCard = document.querySelector(".card").cloneNode(true);
      document.body.appendChild(cloneCard);
      console.log(cloneCard);    
    },

    background() {
      document.querySelectorAll(".card").forEach((item) => {
        if(!item.classList.contains("basic")){
          item.classList.add("basic");
          console.log(item);
        }
        else{
          item.classList.remove("basic");
          console.log(item);
        }
      });
    },

    heading() {
      document.querySelectorAll(".title").forEach((item) => {   
        if(item.innerHTML=="something else"){
          item.innerHTML="Chad of Cyber IST";
        }
        else{
          item.innerHTML="something else";
        }
      });
    },

    //Kinda borked rn
    deleter(){
      document.querySelector(".card:last-child").remove();
      console.log(card);
    }
  }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
