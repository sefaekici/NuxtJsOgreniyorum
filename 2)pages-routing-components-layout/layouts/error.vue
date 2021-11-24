<template>
    <!--
        layouts klasörü içerisinde error.vue adında bir dosya oluşturursak eğer 
        bu sayfa artık varsayılan error page imiz olur. 
    -->
    <div class="errorPage">
        <h1>Hoydaa!!!</h1>
        <p>Bu sayfa bulunamadı.Lütfen Tekrar Deneyiniz!</p>
    </div>
</template>



<style>
    .errorPage{
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>