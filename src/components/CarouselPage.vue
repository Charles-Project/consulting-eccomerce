<template>
    <div class="carousel__wrapper">
      <div class="carousel__content">
         <b-carousel
      id="carousel-1"
      controls
      indicators
      background="#ababab"
      style="text-shadow: 1px 1px 2px #333;"
    >

        <b-carousel-slide>
          <template v-slot:img>
              <img src="../assets/background1.jpg" alt="" srcset="" class="d-block img-fluid w-100">
          </template>
       </b-carousel-slide>
         <b-carousel-slide>
          <template v-slot:img>
              <img src="../assets/background2.jpg" alt="" srcset="" class="d-block img-fluid w-100">
          </template>
       </b-carousel-slide>

       <b-carousel-slide>
          <template v-slot:img>
              <img src="../assets/background4.jpg" alt="" srcset="" class="d-block img-fluid w-100">
          </template>
       </b-carousel-slide>
    </b-carousel>
     </div>
    </div>
</template>

<script>
export default {
    name: "CarouselPage"
}
</script>
<style lang="scss" scoped>
.carousel__wrapper{
 width: 100%;
 padding: 2rem 0;
 /* height: calc(100vh - 60px); */

 display: flex;
 justify-content: center;
 align-items: center;


 .carousel__content{
   
     max-width: 1100px;
     width: 90%;

    
 }


}
</style>