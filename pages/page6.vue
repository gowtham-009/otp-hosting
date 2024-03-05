<template>
    <div class="main-module">
       <div class="sub-contain w-100 d-flex gap-5 p-5">
         <div class="personal-box pb-1  w-25 p-3">
            <div class="personal-link d-flex gap-3 w-100 p-2">
                <div class="pen d-flex justify-content-center align-items-center p-2">
                  <i class="fa-solid fa-pencil text-white  fs-4"></i>                </div>
            <p class="fs-4">Personal</p>
            </div>
         </div>
         <div class="personal-box p-3  w-100">
            <div class="d-flex p-3 line w-100 p-3">
            <div class="title-content-box w-100  p-2 d-flex align-items-center flex-wrap gap-3">
               <p class="fs-5">Welcome</p><h3 class="d-flex bol">VENKATACHALAM,</h3><p class="fs-5 mt-2 p-s">Share a bit about yourself</p>
            </div>
            <div class="title-content-box w-25  p-2 d-flex justify-content-end align-items-center gap-3">
               <div class="question"><i class="fa-solid fa-question text-white"></i></div><i class="fa-solid fa-ellipsis-vertical do fs-3"></i>
            </div>
         </div>
         <div class="container trade-cont">
            <div class="row p-3">
               <div class="col-12 p-3 tb">
                  <p class="text-dark fs-5 fw-bold">Please select your gender</p>
                  <div class="trade-btn mt-3 d-flex flex-wrap gap-2">
                       <!-- btn-1 -->
                     <input class="male-female-input" v-model="get_gender" value="Male" type="radio" id="g-radioButton1" name="g-radioGroup">
                     <label class="male-female-lable" for="g-radioButton1">Male</label>
                     <!-- btn-2 -->
                     <input class="male-female-input" v-model="get_gender" value="Female" type="radio" id="g-radioButton2" name="g-radioGroup">
                     <label class="male-female-lable" for="g-radioButton2">Female</label>
                      <!-- btn-3 -->
                      <input class="male-female-input" v-model="get_gender" value="Others" type="radio" id="g-radioButton3" name="g-radioGroup">
                     <label class="male-female-lable" for="g-radioButton3">Others</label>

                
                  </div>
                  <p class="fs-5">Gender: {{ get_gender }}</p>
               </div>
               <div class="col-12 tb p-3">
                  <p class="text-dark fs-5 fw-bold">Select your marital status</p>
                  <div class="trade-btn mt-3 d-flex flex-wrap gap-2">
                       <!-- btn-1 -->
                       <input class="married-input" v-model="get_martial_status" value="Married" type="radio" id="m-radioButton1" name="m-radioGroup">
                     <label class="married-lable" for="m-radioButton1">Married</label>
                     <!-- btn-2 -->
                     <input class="married-input" v-model="get_martial_status" value="Unmarried" type="radio" id="m-radioButton2" name="m-radioGroup">
                     <label class="married-lable" for="m-radioButton2">Unmarried</label>
                    
                   
                  </div>
                  <p class="fs-5">Married Status: {{ get_martial_status }}</p>
               </div>
           
               <div class="col-12 cont-btn d-flex justify-content-center align-item-center p-3 mt-3">
                  <NuxtLink class="btn otp-btn w-50" to="/page7">Continue</NuxtLink >
               </div>
            </div>
         </div>
         </div>
        
       </div>
       
    </div>
</template>

<script>
   export default{
      data(){
         return{
            get_gender:null,
            get_martial_status:null,
         }
      }
   }
</script>

<style scoped>
 *{
    margin:0%;
    padding: 0%;
    list-style-type: none;
    box-sizing: border-box;
    
 }
 .bol{
   font-weight: 600;
}
 .main-module{
    width: 100%;
    height: 695px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: white;
 }
 .sub-contain{
    height: auto;
    background-color:rgb(253, 253, 240);
 }
 .personal-box{
    background-color: white;
    border-radius: 10px;
 }
 .pen{
    width: 40px;
    height: 40px;
    border-radius: 100%;
    background-color:rgb(81, 0, 157);
 }
 .personal-link{
    background-color: rgb(239, 234, 244);
    border-radius: 10px;
 }
 .personal-link p{
    color: rgb(81, 0, 157);
 }
.title-content-box {
   height: 60px;
}
.question{
    width: 30px;
    height: 30px;
    border-radius: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: gray;

   
}
.line{
   height: 120px;
   border-bottom: 3px solid rgb(239, 234, 244);;
}
.trade-cont{
   width:60%;
}

/* male-female-groups */
.male-female-input[type="radio"] {
      display: none;
    }
    .male-female-lable {
      display: inline-block;
      padding: 10px 20px;
    
       
      color: black; 
        border: 1px solid rgb(167, 167, 167); 
      cursor: pointer;
      border-radius: 20px;
    }

  
    .male-female-input[type="radio"]:checked + .male-female-lable {
      color: aliceblue;
      background-color:blueviolet; /* Set your desired background color for the selected state */
    }
/* married-status-group */
.married-input[type="radio"] {
      display: none;
    }
    .married-lable {
      display: inline-block;
      padding: 10px 20px;
    
       
      color: black; 
        border: 1px solid rgb(167, 167, 167); 
      cursor: pointer;
      border-radius: 20px;
    }

  
    .married-input[type="radio"]:checked + .married-lable {
      color: aliceblue;
      background-color:blueviolet; /* Set your desired background color for the selected state */
    }
.two-trade{
background-color: blueviolet;
}
.tb{
   border-bottom: 2px solid rgb(185, 184, 184);
}
.otp-btn{
   border: none;
   padding: 2%;
   color: white;
   font-size: 20px;
   background-color: blueviolet;
   border-radius: 30px;
}
@media(max-width:1165px){
   .s-p{
      display: none;
   }
}
@media(max-width:992px){
   .main-module{
   width: 100%;
   height: auto;
   display: flex;
   justify-content: center;
   align-items: start;
   background-color: white;
}
   .question{
   
   display: none;
 
 }
 .do{
   display: none;
 }
 .p-s{
   display: none;
 }
 .sub-contain{
   padding: 0% !important;
}
   .main-module{
      align-items: start;
   }
   .pb-1{
      width: 100% !important;
   }
   .sub-contain{
      flex-wrap: wrap;
   }
   .trade-cont{
      width: 100%;
   }
   
}
</style>