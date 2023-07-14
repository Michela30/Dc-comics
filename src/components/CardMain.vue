<script>
//import

   export default {
    data() {
      return{
    
      }
    },
    methods: {
       formatNumber(n){
        const splicedNumber = n.substring(1);
        const formattedNumber = parseFloat(splicedNumber);
        return formattedNumber
       }
    },
    props: {
        cardThumb: String,
        cardSeries: String,
        cardPrice: String
    }
    
  }
</script>


<template>
 
    <div class="single-card">
        <div class="img-card-box">

            <span class="price-ticket" :class="{ 'sale' : formatNumber(cardPrice) < 5}">
                {{cardPrice}}
            </span>

            <img :src="cardThumb" alt="">
        </div>

        <h5>
            {{cardSeries}}
        </h5>

    </div>

</template>



<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.cards-box {
    .single-card {
            width: calc((100% / 6) - 10px);
            margin-top: 20px;
            margin-bottom: 20px;
            height: 120px;
            position: relative;

            .price-ticket {
                position: absolute;
                background-color: yellow;
                bottom: 0;
                font-size: 0.7em;
                font-weight: bold;
                padding: 0 5px;

                &.sale {
                    background-color: green;
                    color: white;
                }
            }

            .img-card-box {
                height: 120px;

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                };
            }

            h5 {
                text-transform: uppercase;
                font-size: 0.7em;
                color: white;
                padding-top: 10px;
            }

        }
}

</style>