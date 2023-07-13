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
                        <div>
                            image
                        </div>
                        <span>
                            text
                        </span>
                    </div>
                    <div class="card">
                        <div>
                            image
                        </div>
                        <span>
                            text
                        </span>
                    </div>
                    <div class="card">
                        <div>
                            image
                        </div>
                        <span>
                            text
                        </span>
                    </div>
                    <div class="card">
                        <div>
                            image
                        </div>
                        <span>
                            text
                        </span>
                    </div>
                    <div class="card">
                        <div>
                            image
                        </div>
                        <span>
                            text
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
    padding-top: 35px;

    .card{
        width: calc(100% / 5);
        display: flex;
    }
    >* {
        padding: 0 15px;
    }
    
}

</style>