<template>
    <div class="itmes_wrapper">
          <div class="product__items" v-for="product in  products" :key="product">
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
</template>
<script>

import Bag from "../assets/bag.jpg"
import Jumpsuit from "../assets/jumpsuit.jpg"
import Shirt from "../assets/shirt3.jpg"
import Watch from "../assets/smartwatch.jpg"
export default {
    name: 'ProductMerchants',
    data() {
        return{
                  products: [
               {
                   id: 1,
                   title: "Smart Watches",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android",
                   photo: Watch,
                   price: 1000,
                   likes: "140",
                   category: "product_merchants"
               },

               {
                   id: 2,
                   title: "Konye Bags",
                   content: "Good leather bag, for public events and casual events",
                   photo: Bag,
                   price: 3000,
                   likes: "200",
                   category: "product_merchants"
               },

               {
                   id: 3,
                   title: "Venice Wears",
                   content: "Venice Jumpsuit for different occassions, nice and smart",
                   photo: Jumpsuit,
                   price: 1100,
                   likes: "240",
                   category: "product_merchants"
               },

               {
                   id: 4,
                   title: "Venice Wear",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android.",
                   photo: Shirt,
                   price: 500,
                   likes: "229",
                   category: "product_merchants"
               },

                {
                   id: 5,
                   title: "Smart Watches",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android",
                   photo: Watch,
                   price: 1000,
                   likes: "140",
                   category: "product_merchants"
               },

               {
                   id: 6,
                   title: "Konye Bags",
                   content: "Good leather bag, for public events and casual events",
                   photo: Bag,
                   price: 3000,
                   likes: "200",
                   category: "product_merchants"
               },

               {
                   id: 7,
                   title: "Venice Wears",
                   content: "Venice Jumpsuit for different occassions, nice and smart",
                   photo: Jumpsuit,
                   price: 1100,
                   likes: "240",
                   category: "product_merchants"
               },

               {
                   id: 8,
                   title: "Venice Wear",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android.",
                   photo: Shirt,
                   price: 500,
                   likes: "229",
                   category: "product_merchants"
               },
            // --------------------------------------------------------------------

                   {
                   id: 9,
                   title: "Katty Shop",
                   content: "Fluffy Yaki Wig",
                   photo: Watch,
                   price: 1000,
                   likes: "140",
                   category: "product_merchants"
               },

               {
                   id: 10,
                   title: "Konye Bags",
                   content: "Good leather bag, for public events and casual events",
                   photo: Bag,
                   price: 3000,
                   likes: "200",
                   category: "product_merchants"
               },

               {
                   id: 11,
                   title: "Venice Wears",
                   content: "Venice Jumpsuit for different occassions, nice and smart",
                   photo: Jumpsuit,
                   price: 1100,
                   likes: "240",
                   category: "product_merchants"
               },

               {
                   id: 12,
                   title: "Venice Wear",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android.",
                   photo: Shirt,
                   price: 500,
                   likes: "229",
                   category: "product_merchants"
               },

                {
                   id: 13,
                   title: "Smart Watches",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android",
                   photo: Watch,
                   price: 1000,
                   likes: "140",
                   category: "product_merchants"
               },

               {
                   id: 14,
                   title: "Konye Bags",
                   content: "Good leather bag, for public events and casual events",
                   photo: Bag,
                   price: 3000,
                   likes: "200",
                   category: "product_merchants"
               },

               {
                   id: 15,
                   title: "Venice Wears",
                   content: "Venice Jumpsuit for different occassions, nice and smart",
                   photo: Jumpsuit,
                   price: 1100,
                   likes: "240",
                   category: "product_merchants"
               },

               {
                   id: 16,
                   title: "Venice Wear",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android.",
                   photo: Shirt,
                   price: 500,
                   likes: "229",
                   category: "product_merchants"
               },
           ],
        }
    }
}
</script>

<style lang="scss" scoped>

 .itmes_wrapper{
         display: grid;
        grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
         justify-content: center;
         grid-gap: 13px;

      .product__items{
        margin-bottom: 20px ;

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
    background: chartreuse;
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