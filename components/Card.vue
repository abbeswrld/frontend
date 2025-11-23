<template>
    <div class="third content">
        <h1>Что то</h1>
        <img class="ribombee" src="/images/some-stuff/icon2.png" alt="Icon">
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/styles/mixins' as *;


.content {
    margin-left: 50px;
}

.third{
    width: 100%;
    height: 500px;
    background-color: #2E8B57;
    margin-right: auto;
    border-radius: 20px;
}

.third h1{
    padding: 20px;
    margin: 20px;
}

.ribombee{
    width: 90px; 
    margin: 20px;
}

</style>