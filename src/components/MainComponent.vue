<script>
//import
import CardMain from '../components/CardMain.vue'

   export default {
    data() {
      return{
        service:[
            {
                image: 'buy-comics-digital-comics.png',
                text: 'Digital Comics'
            },
            {
                image: 'buy-comics-merchandise.png',
                text: 'Dc Merchandise'
            },
            {
                image: 'buy-comics-subscriptions.png',
                text: 'Subscription'
            },
            {
                image: 'buy-comics-shop-locator.png',
                text: 'Comic Shop Locator'
            },
            {
                image: 'buy-dc-power-visa.svg',
                text: 'Dc Power Visa'
            },

        ],
        cardsObject: [
            {
                thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                price: "$19.99",
                series: "Action Comics",
                type: "comic book",
            },
            {
                thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                price: "$3.99",
                series: "American Vampire 1976",
                type: "comic book",
            },
            {
                thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                price: "$16.99",
                series: "Aquaman",
                type: "graphic novel",
            },
            {
                thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                price: "$2.99",
                series: "Batgirl",
                type: "comic book",
            },
            {
                thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                price: "$3.99",
                series: "Batman",
                type: "comic book",
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                price: "$2.99",
                series: "Batman Beyond",
                type: "comic book",
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                price: "$3.99",
                series: "Batman/Superman",
                type: "comic book",
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                price: "$4.99",
                series: "Batman/Superman Annual",
                type: "comic book",
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                price: "$5.99",
                series: "Batman: The Joker War Zone",
                type: "comic book",
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                price: "$6.99",
                series: "Batman: Three Jokers",
                type: "comic book",
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                price: "$4.99",
                series: "Batman: White Knight Presents: Harley Quinn",
                type: "comic book",
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                price: "$16.99",
                series: "Catwoman",
                type: "graphic novel",
            },
        ]
      }
    },
    methods: {
        getImagePath: function(image){
            return new URL (image, import.meta.url).href;
        }

    },
    components: {
        CardMain
    }
    
  }
</script>


<template>
    <main>

        <section class="jumbotron">
            
            <h3 class="current-series">
                current series
            </h3>
        
        </section>

        <section>

            <div class="main-top">
                <div class="main-container">
    
                    <div class="cards-box">

                        <CardMain v-for="(singleCard,i) in cardsObject" :key="i"
    
                        :cardThumb="singleCard.thumb"
                        :cardPrice="singleCard.price"
                        :cardSeries="singleCard.series"/>
    
                        <button>
                            <a href="#">
                                LOAD MORE
                            </a>
                        </button>
                                            
                    </div>

                </div>
            </div>
            
        </section>

        <section class="main-bottom">
            <div class="main-container">
                <div class="row_service">
           
                    <div class="service" v-for="(singleElement,i) in service" :key="i">

                        <div class="service-img-container">
                            <img :src="getImagePath(`../assets/img/${singleElement.image}`)" alt="">
                        </div>
                        <span>
                            {{singleElement.text}}
                        </span>

                    </div>

                </div> 

            </div>
        </section>

    </main>

</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.jumbotron {
    width: 100%;
    height: 250px;
    background-image: url(../assets/img/jumbotron.jpg);
    background-position: top;
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;
    .current-series {
        position: absolute;
        z-index: 2;
        left: 300px;
        bottom: -15px;
        padding: 10px;
        background-color: $main-bg-color;
        color: white;
        text-transform: uppercase;
        font-size: 0.8em;
    }
}

.main-top {
    background-color: #1C1C1C;
    padding: 15px 0 0;


    .cards-box{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        margin: 10px;
    }
}

.main-bottom {
    background-color: $main-bg-color;
    height: 120px;

    >* {
        padding: 40px 20px;
    }
}

button {
    margin-top: 40px;
    background-color: $main-bg-color;
    font-size: 0.6em;
    border: none;
    padding: 5px 25px;
    cursor: pointer;

    a {
        color: white;
        text-decoration: none;
        font-weight: bold;
    }
}

.row_service {
    display: flex;
    flex-wrap: nowrap;
    justify-content: space-between;
    align-items: center;

    .service {
        width: calc(100% / 5);
        display: flex;

        .service-img-container {
            width: 40px;
            height: 40px;
            
            
            img {
                width: 100%;
                height: 100%;
                object-fit: contain;
            }
        }
        span {
            text-transform: uppercase;
            font-size: 0.6em;
            line-height: 40px;
            margin-left: 0;
        }
    }
    
}

</style>