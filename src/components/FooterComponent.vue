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
                        <!-- lista 2 -->
                       <div>
                           <ul>
                               <h4>
                                   shop
                               </h4>
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


                    <!-- lista 3 -->
                    <div>
                        <ul>
                            <h4>
                                dc
                            </h4>
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
                            <li>
                                <a href="#">
                                    link
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

                <div class="logo-big">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>

        </div>
        
        <div class="footer-bottom">
            <div class="main-container">

                <div class="footer-bottom-row">

                    
                    <div class="footer-button">
                        
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

                        <span class="icon-circle">
                            <i class="fa-brands fa-facebook-f"></i>
                        </span>
                        <span class="icon-circle">
                            <i class="fa-brands fa-twitter"></i>
                        </span>
                        <span class="icon-circle">
                            <i class="fa-brands fa-youtube"></i>
                        </span>
                        <span class="icon-circle">
                            <i class="fa-brands fa-pinterest-p"></i>
                        </span>
                        <span class="icon-circle">
                            <i class="fa-solid fa-location-dot"></i>
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
    @include footer-debug
}

.footer_row{
    display: flex;
    align-items: center;
}

.lists{
    display: flex;
}

.firstlist{
    margin-left: 20px;
}

ul{
    padding: 0 15px;
    h4{
        text-transform: uppercase;
        color: white;
        padding-bottom: 5px;
    }
    
    li{
        list-style-type: none;
        font-size: 0.7em;

        a{
            color: #555555;
        }
    }
}

.logo-big{
    height: 250px;
    width: 350px;

    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
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

.footer-button{
    margin-left: 0;
    padding: 12px 0;
        a{
            text-decoration: none;

            button{
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

.footer-icons{
    margin-right: 0;
    padding: 20px 0;
    display: flex;

    h4{
        text-transform: uppercase;
        color: $color-link;
        line-height: 25px;
    }
    .icon-circle{
        width: 25px;
        height: 25px;
        border-radius: 50%;
        background-color: #797979;
        text-align: center;
        margin-left: 10px;

        i{
            line-height: 25px;
            color: $footer-bg-color;
        }
    }
}
</style>