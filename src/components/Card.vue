<template>
  <b-container >
        <b-row class="rowClass edit">
           <div v-for="sharkInfo in sharkNames" :key="sharkInfo">
            <div class="col-12 gridClass">
            <div class="card  ">
               <img class="card-img-top" :src="sharkInfo.img" :alt="sharkInfo.name">
              <div class='card-body cardClass'>
                <h5 class="card-title">{{sharkInfo.name}}</h5>
                
                <button class="btn btn-primary"><router-link :to="{name:'Sharks', params:{name:sharkInfo.urlName,sharkInfo}}"> Read More</router-link></button>
                <!-- <router-link class="btn btn-primary">Read More</router-link>
                <a href="#" class="btn btn-primary">Read More</a> -->
              </div>
            </div>
          </div>
           </div>
          
        </b-row>
      </b-container>
</template>

<script>
export default {
data(){
    return{
      sharkNames: [
        {name:"Great White", urlName:"greatwhite", info:["Between the male and female, the females tend to be larger.","These sharks can migrate from very long distances such as from Mexico to Hawaii or even longer!", "Due to the size and perceived threats, many people are afraid of great white sharks, thus leading to possible extinction in the future.","These sharks tend to hunt through ambushes.","Great white sharks are impossible to keep in captivity, with the longest being 16 days in Sea World before being released due to it refusing to eat."], located:["Pacific Ocean", "South Africa","Around islands near California", "South Africa", "Australia"], img:"https://media.istockphoto.com/photos/great-white-shark-smile-picture-id533130811?k=6&m=533130811&s=612x612&w=0&h=OzxIzgn7VeKJXlUOv_atT6A_dqywwAlnUU66Y_UU_lc=", summary:"Great white sharks are one of the largest known predatory fish in our waters. They tend to feed on nearly anything from small to large prey. They are very large torpedo like fishes that can reach upto 20ft long and weight over 3000lb. Due to their size they have very few natural predators besides orcas. These sharks stay around temperate waters and usually near shores where there are more prey."},


        {name:"Whale Shark", urlName:"whaleshark",info:["These large beasts are docile creatures and have been known to play with divers.", "Considered endangered and vulnerable.", "Eat by filter feeding."], located:["Australia", "Thailand", "Mexico"], img:"https://media.istockphoto.com/photos/whale-shark-in-brothers-island-red-sea-egypt-picture-id179066402?k=6&m=179066402&s=612x612&w=0&h=BXG9SJuwoiWXhlgeRxuoB_o_muS55-airDDGbomVkyk=", summary:"Whale sharks are enormous fishes that can reach upto 50ft in length and nearly 40000 lb. These docile creatures have been known to swim with divers but it is looked down upon for the divers safety by many scientists. These sharks have pale markings and dots across their body. These sharks tend to swim with their mouth open to feed on small creatures in the ocean."},


        {name:"Tiger Shark", urlName:"tigershark", info:["Tiger sharks are aggressive and have ate even garbage and trash.", "Tiger sharks can give birth upto 80+ small young.","Located near tropical and temperate waters around the world.", "Tiger sharks stripes on the side of their body just like tiger feline cats."], located:["Gulf of Mexico", "North American beaches","Bahamas","Carribbean","Indian Ocean", "Atlantic"], img:"https://media.istockphoto.com/photos/tigershark-lady-picture-id1219251623?k=6&m=1219251623&s=612x612&w=0&h=jw0OsRJnAMFlD6rNExOOiwJCCJG1tKi3JmRN2U-iX6g=", summary:"Tiger sharks are known to be voracious predators eating a wide range of food. Essentially what they can get ahold of in their vicinity. Tiger sharks are dangerous near humans but the chance of an attack is very low. These large beasts can grow to be 18 feet and nearly 2000 lb. They like to cruise near open coast and coral-reefs."},


        {name:"Mako Shark", urlname:"makoshark", info:["Do not have any other natural predator.","Have a special blood vessel structure that allows the mako shark to maintain a body temperature greater than the water they are currently in.", "Mako sharks have the largest brain to body ratio of all sharks.", "Considered warm blooded.", "Considered a vulnerable species due to how valuable their fins are to fisherman."], located:["Gulf of Mexico & around Texas","Carribbean","Atlantic","Florida"], img:"https://media.istockphoto.com/photos/shortfin-mako-shark-isurus-oxyrinchus-off-cape-point-south-africa-picture-id1126680005?k=6&m=1126680005&s=612x612&w=0&h=gUINoeRjtDHy42BrKCRKVLowa-XTQaB1YaDBz_xQu20=", summary:"Mako sharks are the fastest of all sharks and reach around 12 ft and 1300 lb. They can zoom around 45 mph and also leap out the water for prey. They tend to occupy a large geographical range, but mostly around tropical waters. The mako appeared around the Paleocene age. Usually these sharks do not view humans as prey, even then they rarely come into contact with humans."}
      ]
    }
  }
}
</script>

<style scoped>
.gridClass{
  margin: 30px auto;
  max-width: 300px;
}
.card{
   background:#29539b;
}
.cardClass{
  letter-spacing: 1px;
  background: rgb(2, 62, 97);
  border:none;
  color: white;
  border-radius: 5px;
}
</style>