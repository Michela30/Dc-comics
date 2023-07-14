<script>
//import

   export default {
    data() {
      return{
    
      }
    },
    methods: {
       
    },
    props: {
        cardThumb: String,
        cardSeries: String
    }
    
  }
</script>


<template>
 
    <div class="single-card">
        <div class="img-card-box">
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
            background-color: lightcoral;

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
                font-size: 0.6em;
                color: white;
                padding-top: 10px;
            }

        }
}

</style>