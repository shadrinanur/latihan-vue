<script setup>
import { ref } from 'vue'

const message = "Hello World"
const rawHtml = "<li>Nomor 1<li>"
const link = "https://vuejs.org/"

let a= 20
let b= 10
let c = a+b

</script>

<template>
  <div id="app">
    <h1>{{ message }}</h1>
    <span v-html="rawHtml"></span>
    <span style="color: blueviolet;">Tulisan ini berwarna ungu</span>
    <div v-bind:id="dynamicId"></div>
    <button v-bind:disabled="isButtonDisabled">Tombol</button>
    <br>
    <a v-on:click="doSomething"> contoh </a>
    <br>
    <a v-bind:href="link">VUE</a>
    <br>
    bilangan 1 = {{ a }} <br>
    bilangan 2 = {{ b }} <br>
    hasil bilangan1 + bilangan2 = {{  c }}
  </div>
</template>