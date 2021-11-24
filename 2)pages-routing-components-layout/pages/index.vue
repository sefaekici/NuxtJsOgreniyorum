<template>
  <section class="container">
    <h1>Anasayfa</h1>
    <p class="content">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quas repellat deleniti blanditiis non. Ipsum, eveniet vitae. Qui velit tempora pariatur adipisci quisquam ad reiciendis? Necessitatibus eveniet nihil quis laudantium ad?
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet, eius facere accusamus aliquid dolore, ipsa perferendis nesciunt illum suscipit dignissimos, reprehenderit molestiae corporis dolor! Temporibus blanditiis consectetur possimus vitae magnam?</p>

    <div class="input-container">
      <input type="text" v-model="itemID">
      <button class="button-green" style="margin-top:12px;" @click="showItems()">Ürünü Göster</button>
    </div>

    <div class="button-container">
      <!--
        Yönlendirme işlemini aşağıdaki gibi a etiketi ile beraber yaparsak sayfa yenilenir 
        Yani server sayfayı yeniler SPA gibi çalışmaz.  
        Bu bir routing olmaz bu server side üzerinden sayfanın yeniden çağırılması olur.
        Sayfanın server üzerinde render edilmesini sağlar 
        nuxt-link ile yapılan yönlendirmeler server üzerinde render edilmez.
      -->
      <a href="/products" class="button-green">Products</a>
      <!--
        nuxt-link kullanıldığında ise direkt olarak yönlendirme işlemini gerçekleştirir.
        tag ise hangi html elementinin domda çizileceğini belirler.
      -->
      <nuxt-link to="/lists" tag="a" class="button-green">Lists</nuxt-link>
      <nuxt-link to="/items" tag="a" class="button-green">Items</nuxt-link>
      <nuxt-link to="/items/1" tag="a" class="button-green">Items Id'li</nuxt-link>
      <nuxt-link to="/users" tag="a" class="button-green">Users</nuxt-link>
      <nuxt-link to="/users/12" tag="a" class="button-green">Users Id'li</nuxt-link>
    </div>   
  </section>
</template>

<script>
export default {
  data(){
    return{
      itemID:"",
    }
  },
  methods:{
    showItems(){
      //js ile router pushlama işlemi
      this.$router.push("/items/"+this.itemID);
    }
  }
}
</script>


<style>
 .container{
   min-height: 100vh;
   padding: 0px 30px;
   text-align: center;
   display: flex;
   flex-direction: column;
   align-items: center;
   justify-content: center;
 }
  a{
    text-decoration: none;
  }
  .button-container{
    border: 1px solid #392;
    background-color: #dedede;
    padding: 20px;
    box-shadow: 2px 3px 8px rba(0,0,0,.1);
    margin-top: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .button-green{
    width: 100px;
    height: 40px;
    color: green;
    border: 2px solid green;
    padding: 5px;
    margin-left: 5px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 5px;
  }
</style>