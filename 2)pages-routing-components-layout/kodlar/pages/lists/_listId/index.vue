<template>
    <div class="container">
        <!--
            id parametresinin ismini içinde bulunduğu klasör belirlerdi.
        -->
        <h3>Element Id: {{$route.params.listId}}</h3>


        <div class="button-container">
            <nuxt-link to="/lists" tag="a">Geri Dön</nuxt-link>
            <button class="button-green" @click="editList()">Düzenle</button>
        </div>
    </div>
</template>



<script>
export default {
    //validate methodu nuxt js ile birlikte gelir ve içerisine 1 adet parametre alır.
    validate(arg){
        //Genel olarak route validation için kullanılır.
        console.log("arg:",arg);
        // return true;
        // return arg.params.listId==2; //burada içerisinde koşul verebilir eğer verdiğimiz koşul true dönmezse sayfa colud not error verir 
        return /^\d+$/.test(arg.params.listId); //Bu şekilde regex çalıştırılabilir int olup olmadığını kontrol eder. 
    },
    methods:{
        editList(){
            this.$router.push("/lists/"+ this.$route.params.listId + "/listDetail")
        }
    }
}
</script>