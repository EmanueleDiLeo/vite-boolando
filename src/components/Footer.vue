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
          <li v-for="(social,index) in social"
            :key="index">
            <a :href="social.href"><i :class="social.icon"></i></a>
          </li>
  
          
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
import {social} from '../data/footerMenu';

export default {
  name:'Footer',
  data(){
    return{
      social,
    }
  }
}
</script>

<style lang="scss" scoped>
  @use '../scss/partials/variabiles' as *;
  @use '../scss/partials/utiles' as *;
  @use '../scss/partials/general' as *;
  @use '../scss/partials/typography' as *;

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
  }
}
</style>