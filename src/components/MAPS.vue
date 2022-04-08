<template>
<div class="container-fluid">
    <div class="row">
        <div class="col-12 col-lg-6">
           
            <!-- prvi red -->
            <div class="row">
                <div class="col-12 col-lg-12">
                    <h1 class="h1_location">You can find us on this google map</h1>
                </div>
            </div>
            <!-- drugi red -->
            <div class="row">
                <div class="col-12">
                    <h3 class="h3_location">Register your business in your state and obtain any business permits requires at the local level. Contact your secretary of state to begin the registration process, and contact your county clerk to inquire about permit requirements in your community.</h3>
                </div>
            </div>
             <!-- treci red -->
            <div class="row">
                <div class="col-12">
                    <b><h4 class="adresa">𝙆𝙣𝙟𝙖𝙯𝙖 𝙈𝙞𝙡𝙤𝙨𝙖 𝙗𝙗, 𝙆𝙤𝙨𝙤𝙫𝙨𝙠𝙖 𝙈𝙞𝙩𝙧𝙤𝙫𝙞𝙘𝙖 38228</h4></b>
                    <h3 class="h3_location">
                        Create a business plan and seek funding for your business. A game store generally requires a large upfront investment in inventory, especially in the video game segment, so startup financing is likely an essential component of getting your store in order. Place emphasis on your marketing and financial plans in your business plan, showing that you fully understand your target market, including their evolving preferences and the best ways to reach them with advertising messages, and that you understand where your profit will come from.
                    </h3>
                </div>
            </div>

        </div>
        <div class="col-12 col-lg-6" >
            <iframe class="map_fix" style="margin-top:40px; border-radius:15px" src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d9831.02840799503!2d20.85877020831888!3d42.89854109290712!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1353454173ddac9d%3A0x272dba8d9db866cb!2sVIVA%20Smart%20Shop!5e0!3m2!1sen!2sus!4v1649185085568!5m2!1sen!2sus" width="90%" height="500px" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
    </div>

    <div class="row">
        <br><Footer /> 
    </div>

</div>
</template>

<script> 
import Footer from '@/components/Footer.vue'

export default {
  name: 'MAPS',
  props: {
    msg: String
  },
  components: {
     Footer
  }

}

</script>

<style scoped>

.h1_location{
    margin-top: 30px;
    margin-left:30px;
    font-weight: 700;
    color: rgb(52, 52, 108);
    text-align: center;
    
}

.h3_location{
    margin-top: 20px;
    font-size: 20px;
    text-decoration: none;
    text-align: justify;
    padding-right: 10px;
    padding-left: 30px;
    color: rgb(52, 52, 108);
    font-weight: 800;
}

@media (min-width: 990px){
    .h1_location{
        margin-top: 50px;
        margin-left:30px;
        font-weight: 700;
        color: rgb(52, 52, 108);
        text-align: center;
    }
}

.adresa{
    margin-top: 30px;
    margin-bottom: 30px;
    font-weight: 800;

}

@media (max-width: 1500px){
    .map_fix {
        padding-top:20px;
        height: 700px;
        transition: width 2s;
    }
}
@media (max-width: 1100px){
    .map_fix {
        padding-top:20px;
        height: 750px;
        transition: width 2s;
    }
}


</style>