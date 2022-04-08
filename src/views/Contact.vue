<template>
     <div class="contact">
         <Navbar />
        <br>
    
        <div class="container contact-form" style="border-radius:10px; margin-bottom:-30px ">
            <div class="contact-image">
                <img src="@/assets/imgs/img1.jpg" alt="rocket_contact"/>
            </div>
            <form method="post" style="margin-top:-50px" >
                <h3 style="color:white;text-align: justify;margin-top:-6px">Feel free to contact us if you have some problems with some purchases or if you have some question. We will reply as soon as we can.</h3>
               <div class="row">
                    <div class="col-md-6">
                        <div class="form-group">
                            <input type="text" name="txtName" class="form-control" placeholder="Your Name *" value="" />
                        </div>
                        <div class="form-group">
                            <input type="text" name="txtEmail" class="form-control" placeholder="Your Email *" value="" />
                        </div>
                        <div class="form-group">
                            <input type="text" name="txtPhone" class="form-control" placeholder="Your Phone Number *" value="" />
                        </div>
                        <div class="order form-group">
                            <input type="submit" name="btnSubmit" class="btnContact" value="Send Message" />
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="form-group">
                            <textarea name="txtMsg" class="form-control" placeholder="Your Message *" style="width: 100%; height: 150px;"></textarea>
                        </div>
                    </div>
                </div>
            </form>
        </div>
    
  
        <div class="col-12">
            <Footer />
        </div>
    
        

     </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Footer from "@/components/Footer.vue";
export default {
    name: 'Contact',
    components:{
        Navbar,Footer
    },
    props:{

    },
}
</script>

<style scoped>


.contact-form{
    background: #54a1d4;
    margin-top: 3%;
    margin-bottom: 5%;
    width: 80%;
}
.contact-form .form-control{
    border-radius:1rem;
}
.contact-image{
    text-align: center;
}
.contact-image img{
    border-radius: 6rem;
    width: 11%;
    margin-top: -3%;
    transform: rotate(11deg);
}
.contact-form form{
    padding: 14%;
}
.contact-form form .row{
    margin-bottom: -12%;
}
.contact-form h3{
    margin-bottom: 8%;
    margin-top: -10%;
    text-align: center;
    color: #0062cc;
}
.contact-form .btnContact {
    width: 80%;
    border: none;
    margin-top:20px;
    margin-bottom:10px;
    border-radius: 50px;
    padding: 1.5%;
    background: #dc3545;
    font-weight: 600;
    color: #fff;
    cursor: pointer;
    
}
.btnContactSubmit
{
    width: 50%;
    border-radius: 10px;
    padding: 1.5%;
    color: #fff;
    background-color: #0062cc;
    border: none;
    cursor: pointer;
    
}
.form-group{
    margin-top: 10px;
}

@import'~bootstrap/dist/css/bootstrap.css';
</style>