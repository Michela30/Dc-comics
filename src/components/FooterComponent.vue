<script>
//import

   export default {
    data() {
      return{
        linkListUno: [
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
                nome: 'News',
                link: '',
            },

        ],
        linkListDue: [
            {
                nome: 'Shop DC',
                link: '',
            },
            {
                nome: 'Shop DC Collectibles',
                link: '',
            },
        ],
        linkListTre: [
            {
                nome: 'Terms of Use',
                link: '',
            },
            {
                nome: 'Privacy policy',
                link: '',
            },
            {
                nome: 'Ad Choices',
                link: '',
            },
            {
                nome: 'Advertising',
                link: '',
            },
            {
                nome: 'Jobs',
                link: '',
            },
            {
                nome: 'Subscriptions',
                link: '',
            },
            {
                nome: 'Talent Workshop',
                link: '',
            },
            {
                nome: 'CPSC Cetficates',
                link: '',
            },
            {
                nome: 'Rating',
                link: '',
            },
            {
                nome: 'Shop Help',
                link: '',
            },
            {
                nome: 'Contact Us',
                link: '',
            },
        ],
        linkListQattro: [
        {
                nome: 'DC',
                link: '',
            },
            {
                nome: 'MAD Magazine',
                link: '',
            },
            {
                nome: 'DC Kids',
                link: '',
            },
            {
                nome: 'DC Universe',
                link: '',
            },
            {
                nome: 'DC Power Visa',
                link: '',
            },
        ],
        iconImage: [
            {
                image: 'footer-fb.png',
                link: ''
            },
            {
                image: 'footer-twitterNew.png',
                link: ''
            },
            {
                image: 'footer-youtubeNew.png',
                link: ''
            },
            {
                image: 'footer-pinterestNew.png',
                link: ''
            },
            {
                image: 'footer-periscopeNew.png',
                link: ''
            },
        ]
      }
    },
    methods: {
        getImagePath: function(image){
            return new URL (image, import.meta.url).href;
        }
    }
    
  }
</script>


<template>
    <footer>
        <div class="container">
            
            <div class="footer_row">
                <div class="lists">
                    <!-- lista 1 -->
                    <div class="firstlist">
                        <ul>
                            <h4>
                                dc comedies
                            </h4>
                            <li v-for="links in linkListUno">
                                <a href="#" >
                                    {{links.nome}}
                                </a>
                            </li>
                        </ul>
                        <!-- lista 2 -->
                       <div>
                           <ul>
                               <h4>
                                   shop
                               </h4>
                               <li v-for="links in linkListDue">
                                   <a href="#">
                                    {{links.nome}}
                                   </a>
                               </li>
                           </ul>
                       </div> 
                    </div>


                    <!-- lista 3 -->
                    <div>
                        <ul>
                            <h4>
                                dc
                            </h4>
                            <li v-for="links in linkListTre">
                                <a href="#">
                                    {{ links.nome }}
                                </a>
                            </li>
                        </ul>
                    </div>
                
                    <!-- lista 4 -->
                    <div>
                        <ul>
                            <h4>
                                sites
                            </h4>
                            <li v-for="links in linkListTre">
                                <a href="#">
                                    {{ links.nome }}
                                </a>
                            </li>
                        </ul>
                    </div>

                </div>

                <div class="logo-big">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>

        </div>
        
        <div class="footer-bottom">
            <div class="main-container">

                <div class="footer-bottom-row">

                    
                    <div class="footer-left">
                        
                        <a href="#">
                            <button>
                                SIGN-UP NOW!
                            </button>
                        </a>
                            
                    </div>
    
                    <div class="footer-icons">
                        <h4>
                            follow us
                        </h4>

                        <span class="icon-circle" v-for="icon in iconImage">
                            
                            <a href="">
                                <img :src="getImagePath(`../assets/img/${icon.image}`)">
                            </a>

                        </span>
                    </div>
                
                </div>
            </div>
        </div>
    </footer>

</template>



<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

footer{
    height: 250px;
    background-image: url(../assets/img/footer-bg.jpg);
}

.footer_row {
    display: flex;
    align-items: center;
    
    .lists {
        display: flex;
        .firstlist {
            margin-left: 70px;
        }
    }
    
    
    ul {
        padding: 10px 15px;
        h4 {
            text-transform: uppercase;
            color: white;
            padding-bottom: 5px;
        }
        
        li {
            list-style-type: none;
            font-size: 0.7em;

            a {
                color: #555555;
                text-decoration: none;

            }
        }
    }
    
    .logo-big {
        height: 250px;
        width: 400px;
    
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
}

.footer-bottom{
    height: 85px;
    background-color: $footer-bg-color;
    
    .footer-bottom-row{
        display: flex;
        justify-content: space-between;
    }
}

.footer-left {
    margin-left: 0;
    padding: 12px 0;
        a {
            text-decoration: none;

            button {
                background-color: transparent;
                color: white;
                font-size: 0.7em;
                border: none;
                padding: 10px;
                border: 2px solid $border-button;
                cursor: pointer;
            }
        }
}

.footer-icons {
    margin-right: 0;
    padding: 20px 0;
    display: flex;

    h4 {
        text-transform: uppercase;
        color: $color-link;
        line-height: 25px;
    }
    .icon-circle {
        width: 25px;
        height: 25px;
        margin-left: 10px;

        img {
           width: 100%;
        }
    }
}
</style>