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
           
                    <div class="card">
                        <div class="card-img-container">
                            <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                        </div>
                        <span>
                            digital comics
                        </span>
                    </div>
                    <div class="card">
                        <div class="card-img-container">
                            <img src="../assets/img/buy-comics-merchandise.png" alt="">
                        </div>
                        <span>
                            dc merchandise
                        </span>
                    </div>
                    <div class="card">
                        <div class="card-img-container">
                            <img src="../assets/img/buy-comics-subscriptions.png" alt="">
                        </div>
                        <span>
                            subscription
                        </span>
                    </div>
                    <div class="card">
                        <div class="card-img-container">
                            <img src="../assets/img/buy-comics-shop-locator.png" alt="">
                        </div>
                        <span>
                            comic shop locator
                        </span>
                    </div>
                    <div class="card">
                        <div class="card-img-container">
                            <img src="../assets/img/buy-dc-power-visa.svg" alt="">
                        </div>
                        <span>
                            dc power visa
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
}

.row_card{
    display: flex;
    flex-wrap: nowrap;
    justify-content: space-between;
    align-items: center;
    padding-top: 35px;

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
            line-height: 35px;
            margin-left: 0;
        }
    }
    
}

</style>