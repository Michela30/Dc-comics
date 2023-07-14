<script>
//import

   export default {
    data() {
      return{
        cardContent:[
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
    <main>
        <section>

            <div class="main-container">
    
                <div class="main-top">
                    Content goes here 
                </div>
    
            </div>
            
        </section>

        <section class="main-bottom">
            <div class="main-container">
                <div class="row_card">
           
                    <div class="card" v-for="(singleElement,i) in cardContent" :key="i">

                        <div class="card-img-container">
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

main{
    background-color: black;
    color: white;
}
.main-top{
    height: 80px;
    line-height: 80px;
}

.main-bottom{
    background-color: $main-bg-color;
    height: 120px;

    >*{
        padding: 40px 20px;
    }
}

.row_card{
    display: flex;
    flex-wrap: nowrap;
    justify-content: space-between;
    align-items: center;

    .card{
        width: calc(100% / 5);
        display: flex;

        .card-img-container{
            width: 40px;
            height: 40px;
            
            
            img{
                width: 100%;
                height: 100%;
                object-fit: contain;
            }
        }
        span{
            text-transform: uppercase;
            font-size: 0.6em;
            line-height: 40px;
            margin-left: 0;
        }
    }
    
}

</style>