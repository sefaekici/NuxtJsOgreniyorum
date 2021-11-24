
<template>
    <!--
    Vue dosyasının ismi alt çizgi ile başlarsa o dosya id parametresini 
    aldığında çalışıcak dosya olarak Nuxt tarafından tanınır.

    Burada kullanılan itemsId ismi dosyanın adından gelir parametre bu dosya adı ile 
    beraber isimlendirilir.
    -->
    <div class="container">
        <h2>Idli Item {{ $route.params.itemsId}} </h2>
    </div>
</template>



