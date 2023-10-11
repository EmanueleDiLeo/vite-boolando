<template>
  <header>
    <div class="container flex">
    <nav class="main-menu">
      <ul class="flex">
        <li v-for="(filter, index) in filters"
          :key="index">
          <a :href="filter.href"><strong>{{ filter.text }}</strong></a>
        </li>
      </ul>
    </nav>
    <img src="/public/boolean-logo.png" alt="logo" title="logo">
    <nav class="shop-menu">
      <ul class="flex">
        <li v-for="(element,index) in profile"
          :key="index">
        <a :href="element.href"><i :class="element.icon"></i></a>
      </li>

      </ul>
    </nav>
  </div>
  </header>
</template>

<script>
  import {filters , profile} from '../data/headerMenu';

  export default {
    name:'Header',
    data(){
      return{
        filters,
        profile
      }
    }
  }
  </script>

<style lang="scss" scoped>

@use '../scss/partials/variabiles' as *;
@use '../scss/partials/utiles' as *;
@use '../scss/partials/general' as *;
@use '../scss/partials/typography' as *;

header{
  padding-top: 20px;
  padding-bottom: 20px;
  position: fixed;
  top: 0;
  width: 100%;
  background-color:$bg-header-color;
  z-index: 999;
  border-bottom: 1px solid rgba(0, 0, 0, 0.5);
  div{
    justify-content: space-between;
    align-items: center;
    img{
      max-height: 30px;
    }
    nav{
      width: 30%;
    }
  }
}
.main-menu a:hover{
  text-decoration: underline;
}

.shop-menu ul{
  justify-content: flex-end;
}
</style>