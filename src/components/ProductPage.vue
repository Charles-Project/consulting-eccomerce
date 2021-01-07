<template>
    <div class="product__wrapper">
       <div class="product__content">

        <!-- ------------------------------------------------ -->
        <div class="product__selection">
            <div class="custom__select--wrapper">
                <select class="custom-select" @change="onChange($event)"  v-model="selectValue">
                <option v-for="(category) in categories" :key="category.id" :value="category.content">{{category.content}}</option>
                </select>
            </div>

            <div class="product_sortby">
                <h6>Sort By: </h6>
                <button class="btn__sortBy ml-2" @click="handlerHigh">Price - High To Low</button>
                 <button class="btn__sortBy" @click="handlerLow">Price - Low To High</button>
            </div>
        </div>

        <!-- ------------------------------------------------ -->

        <h6 class="product__category">{{title}}</h6>
        <!-- ------------------------------------------------ -->
        <div class="itmes_wrapper">
          <div class="product__items" v-for="product in items" :key="product.id">
                    <div class="product-wrapper">
                        <div class="product-cart d-flex justify-content-between">
                            <div class="rating">
                                <i class="fas fa-heart mr-1"></i>
                                <span class="rate">{{product.likes}}</span>
                            </div>
                            <h5 class="discount">${{product.price}}</h5>
                        </div>

                        <div class="product-img mt-1 mb-2">
                            <img :src="product.photo" alt="">
                        </div>
                        <div class="product-body">
                            <div class="div product-Name pt-2">
                                <h5 class="text-center">{{product.content}}</h5>
                            </div>
                            <h6 class="product-type py-2 text-center">{{product.title}}</h6>
                            <div class="addcart-wrapper d-flex justify-content-between align-items-center">
                                <button class="addcart">Buy Now</button>
                                <h6 class="mb-0">
                                    <i class="fas fa-print"></i>
                                    <span>Sent to Cart</span>
                                </h6>
                            </div>
                        </div>
                    </div>
                 
        
        
        
        
        </div>


    </div>
        <!-- ------------------------------------------------ -->

           
       </div>
    </div>
</template>

<script>

export default {
    name: "ProductPage",
    props:["items", "categories", "selectValue", "title"],
    methods:{
        onChange: function (event) {
            this.$emit('handlerSelect', {
                value: event.target.value
            })
        },

        handlerHigh: function () {
            this.$emit('handlerIncrease',{
                value: "high"
            })
           
        },

        handlerLow: function () {
            this.$emit('handlerDecrease',{
                value: "low"
            })
        }
    }
}
</script>

<style lang="scss" scoped>
  

.product__wrapper{
 width: 100%;
 display: flex;
 justify-content: center;
 align-items: center;
 margin-bottom: 1rem;

 
 .product__content{
     max-width: 1100px;
     width: 90%;

     .product__selection{
         margin-bottom: 2rem;
         display: flex;
         
         @media screen and (max-width: "670px") {
             flex-direction: column;
         }

        .custom__select--wrapper{
            width: 50%;
            .custom-select{
             
             width: 200px;
             font-size: 14px;

             &:focus {
                border: none !important;
                 outline: 0;
                 box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);
             }
         }
        }

        .product_sortby{
            flex: 1;
            display: flex;
            justify-content: flex-start;
            align-items: center;

             @media screen and (max-width: "670px") {
             margin-top: 1rem;
            }

            h6{
                font-size: 14px;
                margin-bottom: 0;
            }

            .btn__sortBy{
                background: transparent;
                padding: 4px;
                border: 1px solid lightgray;
                font-size: 13px;
                transition: all 0.4s ease-in-out;
                &:hover{
                    background: lightgray;
                    color: white;
                    font-weight: 500;
                }

            @media screen and (max-width: "370px") {
             font-size: 11px;
            }
               
            }
        }
         
     }

     .product__category{
         margin-bottom: 2rem;
     }

     .itmes_wrapper{
         display: grid;
        grid-template-columns: repeat(auto-fill, minmax(230px, 1fr));
         justify-content: center;
         grid-gap: 13px;
        min-height: 160px;
      .product__items{
        margin-bottom: 20px ;

      }
         
     }
 }
 
}

.product-wrapper {
    background-color: white;
    padding: 15px;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);
    border-radius: 15px;
    display: inline-block;
}

.product-img {
    width: 100%;
    height: 130px;
}

.product-img img {
    width: 100%;
    height: 100%;
  
}

.discount {
    background-color: #ff0476;
    color: white;
    padding: 4px 8px;
    border-radius: 7px;
    appearance: button;
    font-size: 13px;
}

.rating {
    opacity: 0.5;
    font-size: 13px;
}

.product-Name {
    height: 45px;
    border: none;
    border-top: 1px solid #eee;

    
h5 {
    font-weight: 600;
    font-size: 14px;
}
}

.product-type{
    font-size: 14px;
}

.addcart,
.addcart:focus {
    padding: 5px 8px;
    background-color: #00CC6F;
    width: 100%;
    outline: none;
    border: none;
    border-radius: 5px;
    font-size: 12px;
    color: #fff;
    box-shadow: 3px 3px 3px 2px rgba(187, 187, 187, 0.3);

    &:hover {
    color: #00CC6F;
    background-color: transparent;
    border: 1px groove #00CC6F;
    box-shadow: 5px 5px 8px 3px rgba(187, 187, 187, 0.7);
    top: -3px;
}
}



.addcart-wrapper h6 {
    opacity: 0.5;
    display: none;
}


/* product end */




</style>