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
                        <button class="link-button">
                            <a href="#">
                                {{singleLink.nome}}
                            </a>
                        </button>
                    </li>
                  </ul>
              </div>

          </div>

        </div>
    </header>
</template>



<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

header {
    height: 70px;
    padding: 10px 0;
    background-color: white;
    position: relative;
}
.header-top {
    display: flex;
    flex-wrap: nowrap;
    justify-content: space-between;
    align-items: center;
}

.small-logo-container {
    height: 50px;
    width: 50px;
    
    img{
        width: 100%;
    }
}

ul {
    font-size: 0.6em;
    
    li {
        display: inline-block;
        padding: 0 5px;

        button {
            background-color: transparent;
            border: none;
        }
        
        a{
            color: black;
            text-decoration: none;
            text-transform: uppercase;
            font-weight: bold;
        }

        button a:hover {
            border-bottom: 4px solid $color-link;
            color: $color-link;
            padding: 24px 0;
        }
    }
}

</style>