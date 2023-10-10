<template>
  <header>
    <div class="container flex">
    <nav class="main-menu">
      <ul class="flex">
        <li><a href="#"><strong>Donna</strong></a></li>
        <li><a href="#"><strong>Uomo</strong></a></li>
        <li><a href="#"><strong>Bambini</strong></a></li>
      </ul>
    </nav>
    <img src="/public/boolean-logo.png" alt="logo" title="logo">
    <nav class="shop-menu">
      <ul class="flex">
        <li><a href="#"><i class="fa-regular fa-user"></i></a></li>
        <li><a href="#"><i class="fa-regular fa-heart"></i></a></li>
        <li><a href="#"><i class="fa-solid fa-bag-shopping"></i></a></li>
      </ul>
    </nav>
  </div>
  </header>
</template>

<script>
export default {
  name:'Header',
}
</script>

<style lang="scss" scoped>

@use '../scss/partials/variabiles' as *;
@use '../scss/partials/utiles' as *;
@use '../scss/partials/general' as *;

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
      a{
        margin-right: 10px;
      }
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