<template>
         <section class="about">
            <form action="https://t.me/control_ward" target="_blank" method="get">
               <button class="info-tg">
                  <span>Telegram</span>
               </button>
            </form>
         </section>
</template>


<style lang="scss" scoped>
@use '../assets/styles/mixins' as *;


.about {
    width: 100%;
    height: 200px;
    text-align: center;
    display: flex;           
    align-items: center;
    background-color: #4682B4;
    border-radius: 30px;
}

.info-tg{
    width: 256px;
    height: 124px;
    border-radius: 30px; 
    cursor: pointer;
    padding: auto;
    margin-left: 20px;
    position: relative;
    background-color: #26a4e3;
    border: none;
}

.info-tg span { 
    position: absolute;
    bottom: 10px;
    left: 10px;
    font-family: "mine";
    color: white;
    font-size: 40px;
    font-family: mine;
}

.info-tg:hover{
    opacity: 0.9;
    filter: brightness(1.1);
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
}

</style>