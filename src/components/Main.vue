<template>
  <main>
    <div class="container flex">

      <ProductCard 
        v-for="(product,index) in products" :key="index"
          :product="product"/>

    </div>
  </main>
</template>

<script>
import ProductCard from './partials/ProductCard.vue';
import {products} from '../data/mainProducts';

export default {
  name:'Main',
  components:{
    ProductCard,
  },
  data(){
    return{
      products,
    }
  },

}
</script>

<style lang="scss" scoped>
  @use '../scss/partials/variabiles' as *;
  @use '../scss/partials/utiles' as *;
  @use '../scss/partials/general' as *;
  @use '../scss/partials/typography' as *;

  main{
    margin: 150px 0px 30px 0px;
    .container{
      flex-wrap: wrap;
      justify-content: center;
      align-content: start;
    }
  }


</style>