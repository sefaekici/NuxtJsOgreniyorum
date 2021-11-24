<!--
Nuxt js de routelar dosyalar ile yönetilebilir 
Örneğin bu dosyaya http//localhost:3000/products ile erişilebilir 
Aynı şekilde örneğin  http://localhost:3000/products:id olursa 
bir klasör oluşturulur products adında içerisinde _id isimli bir klasör ve 
onunda içerisinde index.vue isimli bir dosya oluşturulmalıdır
index.vue dosyaları ana dizinleri gösterirler.
-->
<template>
    <div class="container">
        <h3>Burası Urun Sayfası</h3>
    </div>
</template>



<script>
export default {
    /*Componentin Hangi Layoutu Kullanıcağı Burada Belirtilir.
      Eğer belirtilmezse default layout kullanılır.
      Ana dizinde bulunan layouts klasörünün içerisinde arar.
      Bütün childlara etki etmesini istiyorsak parent componentte çağırılmalıdır.  
    */
    layout:"product"
}
</script>