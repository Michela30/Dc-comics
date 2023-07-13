<script>
//import

   export default {
    data() {
      return{

      }
    },
    
  }
</script>


<template>
    
    <header>
        <div class="header-container">
    
          <div class="header-top">
              <div class="small-logo-container">
                  <img src="../assets/img/dc-logo.png" alt="">
              </div>

              <!-- questi link saranno ciclati tramite dat() -->
              <div class="links">
                  <ul>
                    <li>
                        <a href="#">
                            link
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            link
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            link
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            link
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            link
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            link
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            link
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            link
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            link
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            link
                        </a>
                    </li>
                  </ul>
              </div>
          </div>
        </div>
      </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

header{
    height: 70px;
    @include header-debug;
}
.header-container{
    max-width: 1100px;
    padding: 10px 0;
}
.header-top{
    display: flex;
    flex-wrap: nowrap;
    justify-content: space-between;
    align-items: center;
}

.small-logo-container{
    height: 50px;
    width: 50px;
    
    img{
        width: 100%;
    }
}

ul{
    font-size: 0.6em;

    li{
        display: inline-block;
        padding: 0 10px;
    }
    a{
        color: black;
        text-decoration: none;
        text-transform: uppercase;
        font-weight: bold;
    }
    &a.active{
        color: $color-link;
        border-bottom: 2px solid $color-link;
    }
}

</style>