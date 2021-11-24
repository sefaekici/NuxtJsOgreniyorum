<template>
    <div class="container">
        <div class="container-2">
            <!--nuxt child sayesinde bir nevi layout yapısı oluşur
            products altında olan bütün childlarda bu kısım gözükür 
            nuxt-child componentinin gözüktüğü yerlerde ise routelardan gelen 
            kısımlar olur.
            Pages ana dizininde tanımlanmak zorundadır.
            -->
            <h3>Burası Layout Kısmı Bütün Lists Componentlerinde Gözükücek</h3>
        </div>
        <nuxt-child></nuxt-child>
    </div>
</template>


<script>
export default {
    layout:"list"
}
</script>