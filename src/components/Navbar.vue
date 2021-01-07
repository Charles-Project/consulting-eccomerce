<template>
    <div class="nav__wrapper">
      <div class="nav_wrapper_header">
           <div class="nav__wrapper--logo">
               <div class="img__logo">
                   <img src="https://9pay.com.ng/newHome/_nuxt/img/9pay_logo.7efbc99.png" alt="" srcset="">
               </div>
           </div>


           <div class="nav_wrapper--search">
              <div class="input-group">
                      <div class="input-group-append">
                        <input type="text" placeholder="Enter your Search" class="nav_wrapper-input" v-model="searchValue">
                    </div>
                    <div class="input-group-append">
                        <button class="btn btn__select" @click="handlerClick"  type="button">Search</button>
                    </div>
                    </div>
           </div>



           <div class="nav__wrapper--body">

            <button class="navbar-toggler mr-3" type="button">
               <i class="fas fa-search"></i>
            </button>


             <button class="navbar-toggler" type="button">
                <i class="fas fa-bars"></i>
             </button>

              <div class="router_wrapper">
                    <router-link to="/" class="nav__link">Login</router-link>
                    <router-link to="/" class="nav__link">SignUp</router-link>
                    <router-link to="/" class="nav__link"> <i class="fas fa-shopping-cart"></i></router-link>
               
              </div>
           </div>
      </div>


      <!--  -->



    </div>
</template>
<script>
export default {
    name: "NavbarWrapper",
    data() {
       return{
            searchValue: ""
       }
    },
    methods:{
        handlerClick: function() {
            this.$emit('searchItem', {
                value:  this.searchValue
            })

            this.searchValue = "";
        }
    }
}
</script>
<style lang="scss" scoped>
.nav__wrapper{
    background-color: #37722D;
    border-color: #37722d;
    height: 60px;
    display: flex;
    justify-content: center;

    .nav_wrapper_header{
        max-width: 1100px;
        width: 90%;
        display: flex;
        justify-content: space-between;

        @media screen and (max-width: 500px) {
            width: 95%;
        }

      
    }
  
}

.nav_wrapper--search{
    /* background: olive; */
    display: flex;
    justify-content: center;
    align-items: center;

    @media screen and (max-width: 700px) {
         display: none;
    }

    .custom_select{
        padding: 0 25px 0 10px !important;
        font-size: 12px !important;
        outline: none !important;
        border: none !important;
    }

    .nav_wrapper-input{
        outline: none !important;
        border: none !important;
        border-left: 1px solid lightgray !important;
        font-size: 13px !important;
        padding: 7px !important;
        width: 300px;
        border-bottom-left-radius: 0.25rem;
        border-top-left-radius: 0.25rem;
    }

    .btn__select{
        background: white;
        font-size: 12px !important;
         border-left: 1px solid lightgray !important;
         padding: 0 10px !important;
         transition: all 0.5s ease-in-out;

         &:hover{
             color: #37722D;
             font-weight: 700;
              transition: all 0.5s ease-in-out;
         }
    }
}

.nav__wrapper--logo{
      /* width: 20%; */
      display: flex;
      justify-content: flex-start;
      align-items: center;


     .img__logo{
        width: 56px;
        height: 44px; 
        
        img{
            /* object-fit: contain; */
            width: 100%;
            height: 100%;
        }
     }
  }

  .nav__wrapper--body{
      /* flex: 1; */
      display: flex;
      justify-content: flex-end;
      align-items: center;

      .navbar-toggler{
          color: white;
          display: none;

          @media screen and (max-width: 700px) {
              display: block;
          }
      }

      .router_wrapper{
    
      display: flex;
      justify-content: flex-end;
      align-items: center;

        @media screen and (max-width: 700px) {
              display: none;
          }

      
      .nav__link{
          color: white;
          text-decoration: none;

          &:hover{
              color: rgb(237, 237, 237);
          }

          &:nth-child(1){
             margin-right: 15px !important; 
          }

           &:nth-child(3){
             margin-left: 15px !important; 
             display: flex;
             align-items: center;
             justify-content: flex-start;
             
             i{
                 font-size: 14px;
             }
           
          }
      }

      }
   
    
  }
</style>