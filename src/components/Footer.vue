<template>
  <footer>
    <div class="container flex">
      <div>
        <h3>Booleando s.r.l</h3>
        <span>Informazioni legali</span>
        <span>Informativa sulla privacy</span>
        <span>Diritto di recesso</span>
      </div>

      <div>
        <span>Trovaci anche su</span>

        <ul class="flex">
          <li><a href="#"><i class="fa-brands fa-twitter"></i></a></li>
          <li><a href="#"><i class="fa-brands fa-square-facebook"></i></a></li>
          <li><a href="#"><i class="fa-brands fa-instagram"></i></a></li>
          <li><a href="#"><i class="fa-brands fa-pinterest"></i></a></li>
          <li><a href="#"><i class="fa-brands fa-youtube"></i></a></li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name:'Footer',
}
</script>

<style lang="scss" scoped>
  @use '../scss/partials/variabiles' as *;
  @use '../scss/partials/utiles' as *;
  @use '../scss/partials/general' as *;

  footer{
  padding:30px 0px 20px 0px;
  background-color: $bg-footer-color;
  color: $link-color;
  .container{
    justify-content: space-between;
    align-items: center;
  }
  span{
    margin-right: 10px;
  }
  h3{
    padding-bottom: 10px;
  }
  ul{
    margin-top: 10px;
    a{
      margin-right: 10px;
    }
  }
}
</style>