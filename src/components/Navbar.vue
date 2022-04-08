<template>
<div class="fixed-top">
<nav class="navbar navbar-expand-xxl navbar-light navbar-banner" >
  <!--  style="background-color: rgba(219, 252, 255)" -->
  <div class="container-fluid">
    <router-link to="/" class="nav-link active">
    <p class="navbar-brand lang namee_store small_push" style="color: rgb(127,, 150, 255)">Apex store</p>
    </router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent" style="padding-top:15px">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item pad-left lang">
          <router-link to="/" class="nav-link active">
          <i class="fa-solid fa-house icons-color fa-beat belo" style="--fa-beat-scale: 1.2; --fa-animation-duration: 3s;font-size:25px"></i>
          </router-link>
          <router-link to="/" class="nav-link active navbar_text_style">Home</router-link>
        </li>
        <li class="nav-item pad-left lang">
          <router-link to="/contact" class="nav-link active">
          <i class="fa-solid fa-address-card fa-beat belo" style="--fa-beat-scale: 1.2; --fa-animation-duration: 3s;font-size:25px"></i>
          </router-link>
          <router-link to="/contact" class="nav-link active navbar_text_style">Contact</router-link> 
          <!-- <a class="nav-link active" aria-current="page" href="#">Contact</a> -->
        </li>
        <li class="nav-item pad-left lang">
          <router-link to="/about" class="nav-link active">
          <i class="fa-solid fa-people-group fa-beat belo"  style="--fa-beat-scale:1.2; --fa-animation-duration: 3s;font-size:25px"></i>
          </router-link>
          <router-link to="/about" class="nav-link active navbar_text_style">About</router-link> 
        </li>
         <li class="nav-item pad-left lang">
           <router-link to="/map" class="nav-link active">
           <i class="fa-solid fa-map-location-dot fa-beat belo" style="--fa-beat-scale: 1.2; --fa-animation-duration: 3s;font-size:25px"></i>
           </router-link> 
          <router-link to="/map" class="nav-link active navbar_text_style">Our location</router-link> 
        </li>
        <li class="nav-item dropdown pad-left lang ">
          <router-link to="" class="nav-link active">
          <i class="fa-solid fa-circle-plus fa-beat belo"  style="--fa-beat-scale: 1.2; --fa-animation-duration: 3s;font-size:25px"></i>
           </router-link>
          <a class="nav-link dropdown-toggle navbar_text_style" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false" style="color:black">Other</a>
          <ul class="dropdown-menu lang-fix" aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item lang aa" target="_blank" href="https://www.origin.com/irl/en-us/store">Origin Store</a></li>
            <li><a class="dropdown-item lang aa" target="_blank" href="https://store.steampowered.com/">Steam Market</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item web-site-lang " target="_blank" href="https://www.gamespot.com/news/">News about games</a></li>
          </ul>
        </li>
      </ul>
      
      <form class="d-flex search_mtop height-search">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button type="submit" class="btn btn-primary">
         <i class="fas fa-search"></i>
        </button>
      </form>
    </div>
  </div>
</nav>
</div>
</template>



<script>

export default {
  name: 'Navbar',
  props: {
    msg: String
  },
  components: {

  }

}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.fixed-top{
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  border-bottom-right-radius: 100%;
}
.navbar_text_style{
font-family: 'Bebas Neue', cursive;
}

.height-search{
  margin-right: 50px;

}

@media (max-width: 1400px){
  .height-search{
    max-width: 50%;
    text-align: center;
    margin: auto;
  }
}

.web-site-lang{
  text-align: center;
  font-weight: bolder;

}
.lang{
  text-align: center;
  
  font-weight: 600;
  font-size: 17px;
  color: black;
  

}
.pad-left{
 margin-left:50px
  
}
.namee_store{
  font-family: 'Rubik Wet Paint', cursive;
  font-size: 50px;
  color: 2c1320;
  
}
.namee_store:hover{
  color:white;
  transition: 0s;
}
/* Za margine na pages */
@media (max-width: 1399px){

.pad-left{
 margin-left: 5px;
  
}
}

/* Za top margin u expand rezimu na search */
@media (max-width: 1400px){

.search_mtop{
  margin-top: 20px;
  
}
}

@media (min-width: 1400px){
.lang-fix{
  margin-right: 50px;
}
}

.navbar-banner{
   background-color: #508bbe;
   font-weight: 300;
   
}

.icons-color{
  color: black;

}

.aa:hover{
  text-decoration: none;
  background: #508bbe;
  transition: 1s;
  border-radius: 10px;
}



@media (max-width: 1000px){
  .small_push{
    margin-left: 100px;
    transition: 1s;
  }
}

@media (max-width: 550px){
  .small_push{
    margin-left: 50px;
    transition: 1s;
  }
}
@media (min-width: 1000px){
  .small_push{
    margin-left: 50px;
    transition: 1s;
  }
}
.belo:hover{
  color: white;
}


</style>
