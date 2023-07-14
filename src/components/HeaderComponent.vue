<script>
//import

   export default {
    data() {
      return{
        headerLinks: [
        {
                nome: 'Characters',
                link: '',
            },
            {
                nome: 'Comics',
                link: '',
            },
            {
                nome: 'Movies',
                link: '',
            },
            {
                nome: 'Tv',
                link: '',
            },
            {
                nome: 'Games',
                link: '',
            },
            {
                nome: 'Collectibles',
                link: '',
            },
            {
                nome: 'Videos',
                link: '',
            },
            {
                nome: 'Fans',
                link: '',
            },
            {
                nome: 'News',
                link: '',
            },
            {
                nome: 'Shop',
                link: '',
            },

        ],
      }
    },
    methods: {
        
    }
    
  }
</script>


<template>
    
    <header>
        <div class="container">
    
          <div class="header-top">
              <div class="small-logo-container">
                  <img src="../assets/img/dc-logo.png" alt="">
              </div>

              <!-- questi link saranno ciclati tramite dat() -->
              <div class="links">
                  <ul>
                    <li v-for="(singleLink, i) in headerLinks">  
                        <a href="#">
                            {{singleLink.nome}}
                        </a>
                    </li>
                    <hr>
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
    padding: 10px 0;
    @include header-debug;
    position: relative;
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
        padding: 0 5px;
        
        a:hover{
            color: $color-link;
            a:hover hr{
                display: block;
            }
        }
    }
    hr{
        position: absolute;
        bottom: 0px;
        width: 5%;
        border: 2px solid $color-link;
        display: none;
    }
    a{
        color: black;
        text-decoration: none;
        text-transform: uppercase;
        font-weight: bold;
    }
}

</style>