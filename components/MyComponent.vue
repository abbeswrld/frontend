
<script setup>
useHead({
  title: 'Главная страница',
  meta: [
    { charset: 'utf-8' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1.0' }
  ],
  link: [
    { rel: 'icon', href: '/images/logo/icon.png' },
    { rel: 'preconnect', href: 'https://fonts.googleapis.com' },
    { rel: 'preconnect', href: 'https://fonts.gstatic.com', crossorigin: '' },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Open+Sans:wght@400;600&display=swap'
    }
  ]
})

import { ref } from 'vue'
import Banner from './Banner.vue'
import Card from './Card.vue'
const greeting = ref('Hello, World!')
function toggleGreeting() {
  greeting.value = greeting.value === 'Hello, World!' ? 'Hello, FEFU!' : 'Hello, World!'
}
</script>

<template>
   <div class="home-page">
      <header>
         <section class="header">
            <h1>Текст хеддера</h1>
         </section>
      </header>

      <main>
         <div class="list content-">
            <h1>Заголовок</h1>
            <ul>
               <li>текст 1</li>
               <li>текст 2</li>
               <li>текст 3</li>
            </ul>
         </div>

         <div class="main content">
            <h1>Заголовок мейн блока</h1>
            <p>{{ greeting }}</p>
            <button @click="toggleGreeting">Сменить приветствие</button>
         </div>

         
         <Card/>

      </main>

      <footer>
        <Banner/>
      </footer>
   </div>

</template>

<style scoped>
:root {
  --font-sans: 'Open Sans', sans-serif;
  --font-heading: 'Montserrat', sans-serif;
}

html{
    font-family: var(--font-sans);
    display: flex;
    flex-direction: column;
    gap: 20px; /* ← расстояние между всеми дочерними элементами */
    padding: 20px;
}

body {
    margin: 0;
    padding: 20px;
    background-color: whitesmoke;
}

button, a, h1, h2 {
    font-family: var(--font-heading)
}

li{
    font-size: larger;
}

main{
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 20px;
}

footer{
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 20px;
}

.home-page{
  width: 100%;
  max-width: 2048px;
  margin: 0 auto;
}

.content-list{
    margin-left: 50px;
    margin-right: 50px;
    justify-content: center;
    align-items: center;
}


.content-main {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: -50px;
    margin-left: 50px;
    margin-right: 50px;
}

.content {
    margin-left: 50px;
}



.header{
    height: 200px;
    width: 100%;
    background-color: aquamarine;
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-left: auto;
    margin-right: auto;
    font-size: large;
}

.list{
    width: 100%;
    height: 500px;
    background-color: #2E8B57;
    margin-left: auto;
    border-radius: 20px;    
}

.list h1{
    padding: 20px;
    margin: 20px;
}

.list ul{
    padding: 20px;
    margin-top: -30px;
    margin-left: 20px;
}

.list li{
    margin-bottom: 10px;
}

.main {
    width: 100%;
    height: 500px;
    background-color: #FFD700;
    margin-right: auto;
    border-radius: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.main h1 {
    padding: 20px;
    margin: 20px;
}

#changeGreetingBtn {
    margin-top: 10px;
    padding: 8px 16px;
    border: none;
    border-radius: 8px;
    background-color: #4682B4;
    color: white;
    cursor: pointer;
}

#changeGreetingBtn:hover {
    background-color: #5a9bd5;
}







</style>
