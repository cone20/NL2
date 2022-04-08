<template >
<div  class="main-page">
<Navbar />

<div class="row " style="margin:2% 1% 0 1%">
  <h1 class="main_text"><b>Welcome to the ApexStore shop</b></h1>

  <div v-for="i in counter"  v-bind:key="i" class="col-12 col-md-6 col-lg-4 col-xl-3 d-flex justify-content-center">
   <Card v-bind:data="card[i-1]" />
  </div>  

</div>

<div class="col-12">
  <button class="load_more load_script" @click="loadMoreItems" >LOAD MORE ITEMS</button>
  <Footer />
  
</div>

</div>
</template>

<script>

import Navbar from '@/components/Navbar.vue'
import Card from '@/components/Card.vue'
import Footer from '@/components/Footer.vue'


export default {
  name: 'Home',
  components: {
    Navbar,Card,Footer
  },
  props: {

  },
  data() {
        return {
            counter: 4,
            card: [
                {
                    id: 1,
                    name: 'GTA V',
                    image: "https://upload.wikimedia.org/wikipedia/en/a/a5/Grand_Theft_Auto_V.png",
                    description: 'Neque porro quisquam est qui dolorem ipsum quia dolor sit amet',
                    price: 34.99,
                    author: 'RockStar',
                    stocks: 10,
                    link: 'https://www.rockstargames.com/gta-v'
                    

                },
                {   
                    id: 2,
                    name: 'Apex Legends',
                    image: 'https://upload.wikimedia.org/wikipedia/en/thumb/d/db/Apex_legends_cover.jpg/220px-Apex_legends_cover.jpg',
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    price: 19.99,
                    author: 'EA',
                    stocks: 24,
                    link: 'https://www.ea.com/games/apex-legends'
                    

                },
                {   
                    id: 3,
                    name: 'Midnight Ghost Hunt',
                    image: 'https://hb.imgix.net/1bf7b7cfd28f65673a028099f92d5531f2c9a25d.jpg?auto=compress,format&fit=crop&h=353&w=616&s=9421a59b2847658dd08396f381eb48ad@/assets/cards_img/rockstar-avatar.jpg',
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    price: 50.95,
                    author: 'Vaulted Sky Games',
                    stocks: 67,
                    link: 'https://store.steampowered.com/app/915810/Midnight_Ghost_Hunt/'
                    

                },
                {   
                    id: 4,
                    name: 'Elden Ring',
                    image: 'https://image.api.playstation.com/vulcan/ap/rnd/202108/0410/0Jz6uJLxOK7JOMMfcfHFBi1D.png',
                    price: 75.99,
                    stocks: 6,
                    author: 'FromSoftware Inc.',
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    link: 'https://en.bandainamcoent.eu/elden-ring/elden-ring'
                    

                },
                {   
                    id: 5,
                    name: 'Fallout 4',
                    image: 'https://image.api.playstation.com/vulcan/ap/rnd/202009/2419/BWMVfyxONkIAlAJVQd96qPuN.png',
                    price: 9.99,
                    stocks: 72,
                    author: 'Bethesda Game Studios',
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    link: 'https://fallout.bethesda.net/en/games/fallout-4'
                    

                },
                {   
                    id: 6,
                    name: 'CoD: BO III',
                    image: 'https://cdn.europosters.eu/image/750/posters/call-of-duty-black-ops-3-cover-i32831.jpg',
                    price: 24.99,
                    stocks: 5,
                    author: 'Activision',
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    link: 'https://www.callofduty.com/blackops3'
                    

                },
                {   
                    id: 7,
                    name: 'Minecraft',
                    image: 'https://upload.wikimedia.org/wikipedia/en/5/51/Minecraft_cover.png',
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    price: 10.99,
                    author: 'Mojang',
                    stocks: 78,
                    link: 'https://www.minecraft.net/en-us'
                    

                },
                {   
                    id: 8,
                    name: 'RUST',
                    image: 'https://www.wizcase.com/wp-content/uploads/2021/03/ZmFfbF-T_400x400.png',
                    price: 13.99,
                    stocks: 83,
                    author: 'Facepunch Studios',
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    link: 'https://rust.facepunch.com/'
                      

                },
                  {   
                    id: 9,
                    name: 'Stardew Valley',
                    image: 'https://m.media-amazon.com/images/M/MV5BYmZiMWNlOWMtODMyNi00ZThiLTk0ZjYtOTQwMGRiNzE2NjFhXkEyXkFqcGdeQXVyNTgyNTA4MjM@._V1_FMjpg_UX1000_.jpg',
                    price: 12.99,
                    author: 'Sickhead Games',
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    stocks:88,
                    link: 'https://www.stardewvalley.net/'
                                        

                },
                  {   
                    id: 10,
                    name: 'OP PW 4',
                    image: 'https://upload.wikimedia.org/wikipedia/en/b/b7/Pirate_Warriors_4_logo.png',
                    price: 45.99,
                    author: 'Omega Force',
                    stocks: 13,
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    link: 'https://oppw4-20-en.bn-ent.net/'
                                        

                },
                  {   
                    id: 11,
                    name: 'Dead by DayLight',
                    image: 'https://i.pinimg.com/originals/c2/26/70/c226703be9c534fd960290e3d61dd70e.png',
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    price: 17.99,
                    author: 'Microsoft',
                    stocks: 48,
                    link: 'https://deadbydaylight.com/'
                    

                },
                  {   
                    id: 12,
                    name: 'DayZ',
                    image: 'https://image.api.playstation.com/vulcan/ap/rnd/202006/1014/ORrwkbfh9B1OwfQbPGLBsgs7.png',
                    price: 42.99,
                    stocks: 23,
                    author: 'Bohemia Interactive',
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    link: 'https://store.steampowered.com/app/221100/DayZ/'
                    

                },
                {
                    id: 13,
                    name: 'Lost Ark',
                    image: "https://kgo.googleusercontent.com/profile_vrt_raw_bytes_1587514212_1078.jpg",
                    description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                    price: 37.99,
                    author: 'RockStar',
                    stocks: 34,
                    link: 'https://www.playlostark.com/en-us'
                    

                },
                {
                  id:14,
                  name: 'Psychonauts 2',
                  image: 'https://upload.wikimedia.org/wikipedia/en/2/23/Psychonauts_2_cover.png',
                  price: 43.99,
                  author: 'Double Fine',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  stocks: 13,
                  link: 'https://store.steampowered.com/app/607080/Psychonauts_2/'
                },
                 {
                  id:15,
                  name: 'PUBG',
                  image: 'https://m.media-amazon.com/images/I/714vaW2G-ZL._SL1500_.jpg',
                  price: 12,
                  author: 'KRAFTON',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  stocks: 99,
                  link: 'https://na.battlegrounds.pubg.com/'
                },
                 {
                  id:16,
                  name: 'Terraria',
                  image: 'https://img.g2a.com/323x433/1x1x0/terraria-steam-gift-europe/591065f6ae653a5dcf684dca',
                  author: 'Re-Logic',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  price: 8.99,
                  stocks: 73,
                  link: 'https://terraria.org/'
                },
                {
                  id: 17,
                  name: 'GTA V',
                  image: "https://upload.wikimedia.org/wikipedia/en/a/a5/Grand_Theft_Auto_V.png",
                  description: 'Neque porro quisquam est qui dolorem ipsum quia dolor sit amet',
                  price: 34.99,
                  author: 'RockStar',
                  stocks: 10,
                  link: 'https://www.rockstargames.com/gta-v'
                  

                },
                {   
                  id: 18,
                  name: 'Apex Legends',
                  image: 'https://upload.wikimedia.org/wikipedia/en/thumb/d/db/Apex_legends_cover.jpg/220px-Apex_legends_cover.jpg',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  price: 19.99,
                  author: 'EA',
                  stocks: 24,
                  link: 'https://www.ea.com/games/apex-legends'
                  

                },
                {   
                  id: 19,
                  name: 'Midnight Ghost Hunt',
                  image: 'https://hb.imgix.net/1bf7b7cfd28f65673a028099f92d5531f2c9a25d.jpg?auto=compress,format&fit=crop&h=353&w=616&s=9421a59b2847658dd08396f381eb48ad@/assets/cards_img/rockstar-avatar.jpg',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  price: 50.95,
                  author: 'Vaulted Sky Games',
                  stocks: 67,
                  link: 'https://store.steampowered.com/app/915810/Midnight_Ghost_Hunt/'
                  

                },
                {   
                  id: 20,
                  name: 'Elden Ring',
                  image: 'https://image.api.playstation.com/vulcan/ap/rnd/202108/0410/0Jz6uJLxOK7JOMMfcfHFBi1D.png',
                  price: 75.99,
                  stocks: 6,
                  author: 'FromSoftware Inc.',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  link: 'https://en.bandainamcoent.eu/elden-ring/elden-ring'
                  

                },
                {   
                  id: 21,
                  name: 'Fallout 4',
                  image: 'https://image.api.playstation.com/vulcan/ap/rnd/202009/2419/BWMVfyxONkIAlAJVQd96qPuN.png',
                  price: 9.99,
                  stocks: 72,
                  author: 'Bethesda Game Studios',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  link: 'https://fallout.bethesda.net/en/games/fallout-4'
                  

                },
                {   
                  id: 22,
                  name: 'CoD: BO III',
                  image: 'https://cdn.europosters.eu/image/750/posters/call-of-duty-black-ops-3-cover-i32831.jpg',
                  price: 24.99,
                  stocks: 5,
                  author: 'Activision',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  link: 'https://www.callofduty.com/blackops3'
                  

                },
                {   
                  id: 23,
                  name: 'Minecraft',
                  image: 'https://upload.wikimedia.org/wikipedia/en/5/51/Minecraft_cover.png',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  price: 10.99,
                  author: 'Mojang',
                  stocks: 78,
                  link: 'https://www.minecraft.net/en-us'
                  

                },
                {   
                  id: 24,
                  name: 'RUST',
                  image: 'https://www.wizcase.com/wp-content/uploads/2021/03/ZmFfbF-T_400x400.png',
                  price: 13.99,
                  stocks: 83,
                  author: 'Facepunch Studios',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  link: 'https://rust.facepunch.com/'
                    

                },
                {   
                  id: 25,
                  name: 'Stardew Valley',
                  image: 'https://m.media-amazon.com/images/M/MV5BYmZiMWNlOWMtODMyNi00ZThiLTk0ZjYtOTQwMGRiNzE2NjFhXkEyXkFqcGdeQXVyNTgyNTA4MjM@._V1_FMjpg_UX1000_.jpg',
                  price: 12.99,
                  author: 'Sickhead Games',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  stocks:88,
                  link: 'https://www.stardewvalley.net/'
                                      

                },
                {   
                  id: 26,
                  name: 'OP PW 4',
                  image: 'https://upload.wikimedia.org/wikipedia/en/b/b7/Pirate_Warriors_4_logo.png',
                  price: 45.99,
                  author: 'Omega Force',
                  stocks: 13,
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  link: 'https://oppw4-20-en.bn-ent.net/'
                                      

                },
                  {   
                  id: 27,
                  name: 'Dead by DayLight',
                  image: 'https://i.pinimg.com/originals/c2/26/70/c226703be9c534fd960290e3d61dd70e.png',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  price: 17.99,
                  author: 'Microsoft',
                  stocks: 48,
                  link: 'https://deadbydaylight.com/'
                  

                },
                  {   
                  id: 28,
                  name: 'DayZ',
                  image: 'https://image.api.playstation.com/vulcan/ap/rnd/202006/1014/ORrwkbfh9B1OwfQbPGLBsgs7.png',
                  price: 42.99,
                  stocks: 23,
                  author: 'Bohemia Interactive',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  link: 'https://store.steampowered.com/app/221100/DayZ/'
                  

                },
                {
                  id: 29,
                  name: 'Lost Ark',
                  image: "https://kgo.googleusercontent.com/profile_vrt_raw_bytes_1587514212_1078.jpg",
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  price: 37.99,
                  author: 'RockStar',
                  stocks: 34,
                  link: 'https://www.playlostark.com/en-us'
                  

                },
                {
                  id:30,
                  name: 'Psychonauts 2',
                  image: 'https://upload.wikimedia.org/wikipedia/en/2/23/Psychonauts_2_cover.png',
                  price: 43.99,
                  author: 'Double Fine',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  stocks: 13,
                  link: 'https://store.steampowered.com/app/607080/Psychonauts_2/'
                },
                 {
                  id:31,
                  name: 'PUBG',
                  image: 'https://m.media-amazon.com/images/I/714vaW2G-ZL._SL1500_.jpg',
                  price: 12,
                  author: 'KRAFTON',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  stocks: 99,
                  link: 'https://na.battlegrounds.pubg.com/'
                },
                 {
                  id:32,
                  name: 'Terraria',
                  image: 'https://img.g2a.com/323x433/1x1x0/terraria-steam-gift-europe/591065f6ae653a5dcf684dca',
                  author: 'Re-Logic',
                  description: 'Ipsum quia dolor sit amet, consectetur, adipisci velit',
                  price: 8.99,
                  stocks: 73,
                  link: 'https://terraria.org/'
                }
                
            ],
            cardVisible: 4,
            step: 4,


        }
  },
  methods: {
    loadMoreItems(){
        this.counter += 4;
        if(this.counter >= this.card.length){
          document.getElementsByClassName('load_script')[0].style.display = 'none';
        }
      }
  },
  computed: {
  },
}

</script>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgb(153, 25, 25);

}


.load_more {
  border-radius: 15px;
  font-weight: 800;
  min-width: 300px;
  margin-top: 65px;
  margin-bottom: -30px;
  align-items: center;
  appearance: none;
  background-color: #FCFCFD;
  border-width: 0;
  box-shadow: rgba(45, 35, 66, 0.4) 0 2px 4px,rgba(45, 35, 66, 0.3) 0 7px 13px -3px,#D6D6E7 0 -3px 0 inset;
  box-sizing: border-box;
  color: #36395A;
  cursor: pointer;
  display: inline-flex;
  font-family: "JetBrains Mono",monospace;
  height: 48px;
  justify-content: center;
  list-style: none;
  overflow: hidden;
  padding-left: 16px;
  padding-right: 16px;
  position: relative;
  text-align: left;
  text-decoration: none;
  transition: box-shadow .15s,transform .15s;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  white-space: nowrap;
  will-change: box-shadow,transform;
  font-size: 18px;
}

.load_more:focus {
  box-shadow: #D6D6E7 0 0 0 1.5px inset, rgba(45, 35, 66, 0.4) 0 2px 4px, rgba(45, 35, 66, 0.3) 0 7px 13px -3px, #D6D6E7 0 -3px 0 inset;
}

.load_more:hover {
  box-shadow: rgba(45, 35, 66, 0.4) 0 4px 8px, rgba(45, 35, 66, 0.3) 0 7px 13px -3px, #D6D6E7 0 -3px 0 inset;
  transform: translateY(-2px);
}

.load_more:active {
  box-shadow: #D6D6E7 0 3px 7px inset;
  transform: translateY(2px);
}

/* Main naslov css */
.main_text{
  margin-bottom: 40px;
  color: rgb(0, 0, 0);
  font-size: 50px;
  font-weight: 800;
  font-family: 'Courier New', Courier, monospace;
  animation: cool 0.5s ease-in;

}
@keyframes cool {
  0% {font-size: 50px;color: #36395A;font-weight: 800;}
  25% {font-size: 45px;color: white;font-weight: 800;}
  50%  {font-size: 50px; color: white;font-weight: 800;}
  75%  {font-size: 45px; color: white;font-weight: 800;}
  100% {font-size: 50px; color: white;font-weight: 800;}

}
.main_text:hover{
  cursor: pointer;

}



@import'~bootstrap/dist/css/bootstrap.css';
</style>
