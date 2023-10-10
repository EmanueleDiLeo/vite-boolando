<template>
  <main>
    <div class="container flex">


     <div class="card">
        <div class="cont-img">
          <img src="../assets/img/1.webp" alt="levi" title="levi">
          <img class="switch" src="../assets/img/1b.webp" alt="levi" title="levi">
        </div>

        <span class="offer box-position">-50%</span>
        <span class="green box-position">Sostenibilità</span>

        <span class="heart">&hearts;</span>

        <span>Levi's</span>
        <h2>RELAXED FIT TEE UNISEX</h2>
        <span class="price">14,99 &euro; </span>
        <span class="old-price"> 29,99 &euro;</span>
      </div>


    </div>
  </main>
</template>

<script>
import {products} from '../data/mainProducts';

export default {
  name:'Main',
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

      .card{
        position: relative;
        width:calc(100% / 3.3);
        margin-bottom: 60px;
        min-width: 250px;
        margin-right: 20px;
        .cont-img{
          cursor: pointer;

          img{
            left: 0px;
            top: 0px;
            max-width: 100%;
            max-height:auto;
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
    }
  }


</style>