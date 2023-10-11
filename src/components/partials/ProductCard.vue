<template>

  <div class="card">
    <div class="cont-img">
      <img :src="product.img" :title="product.brand">
      <img class="switch" :src="product.imgHover" :alt="product.brand" :title="product.brand">
    </div>

    <span class="offer box-position" v-if="product.discount !== null">{{ product.discount }}</span>
    <span class="green box-position" v-if="product.green !== null">{{ product.green }}</span>

    <span class="heart" 
      @click="product.favorite = !product.favorite"
      :class="{'active': product.favorite === true}"
      >&hearts;
    </span>

    <span>{{ product.brand }}</span>
    <h2>{{ product.name }}</h2>
    <span class="price">{{ product.price }} </span>
    <span class="old-price" v-if="product.priceOld !== null">{{ product.priceOld }}</span>
  </div>

</template>

<script>
export default {
  name:'ProductCard',
  props:{
    product:Object,
  },
}
</script>

<style lang="scss" scoped>
  @use '../../scss/partials/variabiles' as *;
  @use '../../scss/partials/utiles' as *;
  @use '../../scss/partials/general' as *;
  @use '../../scss/partials/typography' as *;
  .card{
    position: relative;
    width:calc(100% / 3 - 20px);
    margin-bottom: 60px;
    min-width: 250px;
    margin-right: 20px;
    .cont-img{
      cursor: pointer;

      img{
        left: 0px;
        top: 0px;
        width: 100%;
      }
      .switch{
        position: absolute;
        display: none;
        z-index: 1;
      }
      &:hover .switch{
        display: block;
      }
    }
    .box-position{
      padding: 3px 8px;
      position: absolute;
      z-index: 2;
      color: white;
    }

    .offer{
      background-color: #ff0000;
      bottom: 110px;
      left: 0px;
    }

    .green{
      background-color: #008000;
      bottom: 110px;
      left: 60px;
    }

    .heart{
      color: black;
      position: absolute;
      font-size: 2.5rem;
      text-align: center;
      padding: 6px 16px;
      background-color: white;
      right: 0;
      top: 10px;
      z-index: 2;
      cursor: pointer;
      &:hover{
        color: red;
      }
      &.active{
        color:red;
      }
      &.active:hover{
        color: black;
      }
    }

    span{
      color: #bbc0c5;
    }

    .price{
      color: #ff0000;
    }

    .old-price{
      text-decoration: line-through;
    }
  }
</style>