<template>
<b-container fluid class="mx-0 px-0">
     <Navbar @searchItem="handlerCHange" />
     <Carousel />
     <ProductPage @handlerSelect="onChange" @handlerIncrease="handlerDecending" @handlerDecrease="handlerAscending" :items="items" 
     :categories="categories" :selectValue="selectValue" :title="title"/>
</b-container>
  
</template>
<script>
import  Carousel from "./components/CarouselPage"
import Navbar from "./components/Navbar"
import ProductPage from "./components/ProductPage"

import Bag from "./assets/bag.jpg"
import Jumpsuit from "./assets/jumpsuit.jpg"
import Shirt from "./assets/shirt3.jpg"
import Watch from "./assets/smartwatch.jpg"
import Hair3 from "./assets/hair3.jpg"
import Hair1 from "./assets/hair1.jpg"
import Hair from "./assets/hair.jpg"
import HardDrive from "./assets/harddrive.jpg"
import Tea from "./assets/tea.jpg"
import Tea1 from "./assets/tea1.jpg"
import Gel from "./assets/gel.jpg"
import Hp from "./assets/hp.jpg"


export default {
  components: {
      Navbar,
     Carousel,
     ProductPage
  },

  data(){
    return{
        selectValue: "All Merchants",
        selected: 0,
        title:"All Merchants",
        categories: [
               {
                   id:1,
                   content: "All Merchants"
               },
               {
                   id:2,
                   content: "Product Merchants"
               },
              {
                   id:3,
                   content: "Service Merchants"
               }
           ],
        productItems: [
               {
                   id: 1,
                   title: "Smart Watches",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android",
                   photo: Watch,
                   price: 1000,
                   likes: "140",
                   category: "Product Merchants"
               },

               {
                   id: 2,
                   title: "Konye Bags",
                   content: "Good leather bag, for public events and casual events",
                   photo: Bag,
                   price: 3000,
                   likes: "200",
                   category: "Product Merchants"
               },

               {
                   id: 3,
                   title: "Nike Wears",
                   content: "Venice Jumpsuit for different occassions, nice and smart",
                   photo: Jumpsuit,
                   price: 1100,
                   likes: "240",
                   category: "Product Merchants"
               },

               {
                   id: 4,
                   title: "Venice Wear",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android.",
                   photo: Shirt,
                   price: 500,
                   likes: "229",
                   category: "Product Merchants"
               },

                {
                   id: 5,
                   title: "Rolex Watches",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android",
                   photo: Watch,
                   price: 1000,
                   likes: "140",
                   category: "Product Merchants"
               },

               {
                   id: 6,
                   title: "Kini Bags",
                   content: "Good leather bag, for public events and casual events",
                   photo: Bag,
                   price: 3000,
                   likes: "200",
                   category: "Product Merchants"
               },

               {
                   id: 7,
                   title: "Uche Wears",
                   content: "Venice Jumpsuit for different occassions, nice and smart",
                   photo: Jumpsuit,
                   price: 1100,
                   likes: "240",
                   category: "Product Merchants"
               },

               {
                   id: 8,
                   title: "Tini Wear",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android.",
                   photo: Shirt,
                   price: 500,
                   likes: "229",
                   category: "Product Merchants"
               },
            // --------------------------------------------------------------------

                   {
                   id: 9,
                   title: "Katty Shop",
                   content: "Fluffy Yaki Wig",
                   photo: Hair3,
                   price: 1000,
                   likes: "140",
                   category: "Service Merchants"
               },

               {
                   id: 10,
                   title: "Nikes Shop",
                   content: "Silky Straight Hair With Free Closure - 6 Bundles",
                   photo: Hair1,
                   price: 8500,
                   likes: "400",
                   category: "Service Merchants"
               },

               {
                   id: 11,
                   title: "Virgin Hair",
                   content: "Curly Virgin Human Hair Wig With Frontal",
                   photo: Hair,
                   price: 13000,
                   likes: "240",
                   category: "Service Merchants"
               },

               {
                   id: 12,
                   title: "Seagate",
                   content: "Seagate 1TB Hard Drive - Backup Plus Slim",
                   photo: HardDrive,
                   price: 1000,
                   likes: "229",
                   category: "Service Merchants"
               },

                {
                   id: 13,
                   title: "Beauty Formulas",
                   content: "Beauty Formulas Tea Tree Peel-off Mask - 50ml",
                   photo: Tea,
                   price: 1800,
                   likes: "140",
                   category: "Service Merchants"
               },

               {
                   id: 14,
                   title: "Oil Unique",
                   content: "Tea Tree Oil For Redness & Bumps - 1.8oz",
                   photo: Tea1,
                   price: 3000,
                   likes: "200",
                   category: "Service Merchants"
               },

               {
                   id: 15,
                   title: "Neutrogena",
                   content: "Neutrogena Hydro Boost Water Gel Cleanser 200ml",
                   photo: Gel,
                   price: 1100,
                   likes: "244",
                   category: "Service Merchants"
               },

               {
                   id: 16,
                   title: "hp",
                   content: "HP Gaming Pavilion 15-8th Gen Intel® Core™ i5-15.6",
                   photo: Hp,
                   price: 500,
                   likes: "229",
                   category: "Service Merchants"

               },
           ],
        items:[
               {
                   id: 1,
                   title: "Smart Watches",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android",
                   photo: Watch,
                   price: 1000,
                   likes: "140",
                   category: "Product Merchants"
               },

               {
                   id: 2,
                   title: "Konye Bags",
                   content: "Good leather bag, for public events and casual events",
                   photo: Bag,
                   price: 3000,
                   likes: "200",
                   category: "Product Merchants"
               },

               {
                   id: 3,
                   title: "Nike Wears",
                   content: "Venice Jumpsuit for different occassions, nice and smart",
                   photo: Jumpsuit,
                   price: 1100,
                   likes: "240",
                   category: "Product Merchants"
               },

               {
                   id: 4,
                   title: "Venice Wear",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android.",
                   photo: Shirt,
                   price: 500,
                   likes: "229",
                   category: "Product Merchants"
               },

                {
                   id: 5,
                   title: "Rolex Watches",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android",
                   photo: Watch,
                   price: 1000,
                   likes: "140",
                   category: "Product Merchants"
               },

               {
                   id: 6,
                   title: "Kini Bags",
                   content: "Good leather bag, for public events and casual events",
                   photo: Bag,
                   price: 3000,
                   likes: "200",
                   category: "Product Merchants"
               },

               {
                   id: 7,
                   title: "Uche Wears",
                   content: "Venice Jumpsuit for different occassions, nice and smart",
                   photo: Jumpsuit,
                   price: 1100,
                   likes: "240",
                   category: "Product Merchants"
               },

               {
                   id: 8,
                   title: "Tini Wear",
                   content: "Water Proof Sport Smart Watch Monitor for IOS and Android.",
                   photo: Shirt,
                   price: 500,
                   likes: "229",
                   category: "Product Merchants"
               },
            // --------------------------------------------------------------------

                   {
                   id: 9,
                   title: "Katty Shop",
                   content: "Fluffy Yaki Wig",
                   photo: Hair3,
                   price: 1000,
                   likes: "140",
                   category: "Service Merchants"
               },

               {
                   id: 10,
                   title: "Nikes Shop",
                   content: "Silky Straight Hair With Free Closure - 6 Bundles",
                   photo: Hair1,
                   price: 8500,
                   likes: "400",
                   category: "Service Merchants"
               },

               {
                   id: 11,
                   title: "Virgin Hair",
                   content: "Curly Virgin Human Hair Wig With Frontal",
                   photo: Hair,
                   price: 13000,
                   likes: "240",
                   category: "Service Merchants"
               },

               {
                   id: 12,
                   title: "Seagate",
                   content: "Seagate 1TB Hard Drive - Backup Plus Slim",
                   photo: HardDrive,
                   price: 1000,
                   likes: "229",
                   category: "Service Merchants"
               },

                {
                   id: 13,
                   title: "Beauty Formulas",
                   content: "Beauty Formulas Tea Tree Peel-off Mask - 50ml",
                   photo: Tea,
                   price: 1800,
                   likes: "140",
                   category: "Service Merchants"
               },

               {
                   id: 14,
                   title: "Oil Unique",
                   content: "Tea Tree Oil For Redness & Bumps - 1.8oz",
                   photo: Tea1,
                   price: 3000,
                   likes: "200",
                   category: "Service Merchants"
               },

               {
                   id: 15,
                   title: "Neutrogena",
                   content: "Neutrogena Hydro Boost Water Gel Cleanser 200ml",
                   photo: Gel,
                   price: 1100,
                   likes: "244",
                   category: "Service Merchants"
               },

               {
                   id: 16,
                   title: "hp",
                   content: "HP Gaming Pavilion 15-8th Gen Intel® Core™ i5-15.6",
                   photo: Hp,
                   price: 500,
                   likes: "229",
                   category: "Service Merchants"

               },
        ],

      
    }
  },

  methods:{
    handlerCHange: function (params) {
       if(params.value==""){
        return
      }
      let value = this.productItems.filter(item => item.title.toLowerCase().includes(params.value.toLowerCase()));
     
      if (value === undefined || value.length == 0) {
        this.title = "No Item Match"
        this.items = value;
        return
      }
      this.items = value;
      this.title = params.value;
     
    },

    handlerDecending: function() {
      this.items.sort((a, b) => b.price - a.price);
    },

    handlerAscending: function() {
      this.items.sort((a, b) => a.price - b.price);
  
    },

    onChange: function (event) {
            this.selectValue = event.value;
            this.title = event.value;
            let search = event.value;
              
            if(search === "All Merchants"){
                this.items = [...this.productItems]
                return 
            }

            if(search === "Service Merchants"){
                this.items = this.productItems.filter(item => item.category === "Service Merchants");
                return
            }

            if(search === "Product Merchants"){
                 this.items = this.productItems.filter(item=>item.category === "Product Merchants")
                 return
            }
    },

  

  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
