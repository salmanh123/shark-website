<template>
  <div>
   <div class="container-left">
     <div class='row'>
        <div class="col-4 columnOne" style="margin-top:10px;">
           <h4>{{sharkInfo.name}} info</h4>
           <div>
              <img class="image" :src="sharkInfo.img" alt="">
           </div>
           <div class="sharkInfo">
              <div v-for="information in sharkInfo.info" :key="information">
                 <ul>
                    <li>
                       <p>{{information}}</p>
                    </li>
                 </ul>
              </div>
              <p class="summaryText">Small Summary</p>
              <div class="summary">
                 <p class="summaryP">{{sharkInfo.summary}}</p>
              </div>
           </div>
           
         </div>
         <div class="col-3 locations" style="margin-top:10px">
            <h4>Locations</h4>
            <div v-for="locations in sharkInfo.located" :key="locations">
               <ul>
                  <li>
                     {{locations}}
                  </li>
               </ul>
            </div>
            
         </div>
     </div>
     
   </div>
   
  </div>
</template>

<script>
export default {
   props:['sharkInfo']
}
</script>

<style>
h4{
   padding: 10px 20px;
   text-transform: uppercase;
   letter-spacing: 1px;
}
li{
   background: rgb(55, 78, 209);
   color: white;
   border-radius: 15px;
   text-align: center;
}
p{
   text-align: center;
   font-size: 15px;
   margin: auto;
   padding: auto;
   
}
.summaryText{
   margin-bottom: 3px;
   font-size: 20px;
   text-transform: uppercase;
   text-align: left;
   padding: 0 30px;
}
.summary{
    max-width: 400px;
    margin: 0 20px;
    padding: 20px 30px;
    color: white;
    background: rgb(55, 78, 209);
    border-radius: 8px;
}
.summaryP{
   text-align: left;
   letter-spacing: .5px;
   font-size: 19px;
   
   
}
.sharkInfo{
   text-align: left;
   margin-left: 50px;
   margin-top: 50px;
}
.image{
   max-width: 400px;
   border-radius: 5px;
}
.locations{
   min-height: 30vh;
   height: 30%;
   background: #4B68FB;
   color: white;
   border-radius: 50px;
}
.columnOne {
    min-height: 100vh;
    height: 100%;
    background: #4B68FB;
    color: white;
    margin: 50px;
    
    border-radius: 50px;
}
</style>