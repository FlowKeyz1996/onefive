<template>
  <q-page class="bg-primary background">
    <section>
    <div class="row">
     <div class=" col q-pt-xl q-ma-xl">

      <div class="text-h3 text-secondary q-pb-lg hero_info">
        <span class="text-secondary text-bold">ONE</span>FIVE.COM
      </div>
      <div>
        <p class="text-secondary text-body1 hero_info_para">Get your freelance service for nothing less than 1500</p>
      </div>
       <q-input
        color="black"
        class="bg-secondary insert"
        filled
        placeholder="enter your email here"
             >
        <template v-slot:prepend>
          <q-icon name="email" />
        </template>
        <template v-slot:append>
          <q-btn  class="btn" label="Get Started"></q-btn>
        </template>
      </q-input>
      <div class= "q-mt-xl q-py-xl app_logo_container">
       <p class="text-body2 text-secondary">Download the  ONEFIVE app</p>
       <q-img src="icons/images/Group (2).png" class="app_image"></q-img>
       <q-img src="/icons/images/Badge.png" class="app_image q-ml-md" ></q-img>
       </div>
      </div>
      <div class="col image_container">
        <q-img alt="hero-image" src="/icons/images/Group 153.png" class="hero_image"></q-img>

      </div>

    </div>

  </section>
  </q-page>

  <div class="services_container">
  <div class="text-h3 text-primary q-pa-md q-mt-xl text-bold">Our Services</div>
  <div class="text-body1 services_para">We provide services to you based on your budget from the comfort of your home</div>
   </div>
   <div class="services_links q-pa-xl ">
      <p>All</p>
      <p>Plumbing</p>
      <p>Electrian</p>
      <p>Remodelling</p>
      <p>Appliance-Repair</p>
      <p>Cleaning</p>
   </div>
  <div class="q-pa-md q-ma-xl">

    <div class="row">
      <div class="col services_img_container">
        <q-img src="/icons/images/Rectangle 23.png" class="services_image"> </q-img>
       <p class="text-white text-body1 paragraph">Carpentry Services</p>
       <q-btn color="primary" label="Primary" class="services_btn"/>
      </div>
      <div class="col services_img_container">
        <q-img src="/icons/images/Rectangle 23.png"> </q-img>
        <p class="text-white text-body1 paragraph"> Car wash Services</p>
        <q-btn color="primary" label="Primary" class="services_btn"/>
      </div>
      <div class="col services_img_container">
        <q-img src="/icons/images/Rectangle 23.png"> </q-img>
         <p class="text-white text-body1 paragraph">Cleaning Services</p>
        <q-btn color="primary" label="Primary" class="services_btn"/>
      </div>
    </div>

  </div>
  <section class=" sect_container ">

    <div class="text-h3 text-primary text-bold work_header">
      How it works
      <p class="text-body1 text-secondary q-py-lg work_para">lorem isum dolor sit amet, consectectur ornare dolor volutpat</p>
    </div>
    <div class="padded">
       <div class="text-h3">
        how are you doing and how is everything
      </div>
      <div>
        <q-img src="/icons/images/Rectangle.png"></q-img>
      </div>
     </div>

  </section>
  <section>

  </section>

</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'PageIndex'
})
</script>



<style scoped>
.btn{
  background-color:#2F4858;
  color:white;
}
.hero_info_para{
  max-width:45%;
  font-size:1.2rem;
}
.app_image{
  width:110px;

}
.app_logo_container{
  margin-top:5rem;
}
/*.image_container{
  padding-top:5rem;
  background-color:#ffffff;
  border-top-left-radius:2000px;
  border-top-right-radius:2000px;
  height:600px;
  margin-top:120px;
  margin-right:20px;
  bottom:80%;
  position:relative;
}*/
.hero_info{
  padding-top:5rem;
}
.hero_image{
 /* display:flex;
  justify-content:center;
  align-items:center;
  margin-top:-60px;
  margin-right:-20px;
  align-items:center;
  padding:5rem 3rem;*/
  height:500px;
  position:relative;
  top:28%;
}
.insert{
 max-width:85%;
 border-radius:10px;
}
.services_container{
  margin-top:10rem;
  display:flex;
  flex-direction:column;
  align-items:center;
  justify-content:center;
}
.services_para{
  color:#2F4858;
  font-size:1.5rem;
  max-width:60%;
  text-align:center;
  line-height:1.5rem;
}
.services_links{
  align-items:center;
  justify-content:center;
  display:flex;
  color:#2F4858;
}
.services_links p{
  margin:3rem;
  padding:.5rem;
  font-size:1rem;



}

.services_links p:hover{
  background-color:#1abc9c;
  border-radius:5px;
  color:#ffff;

  cursor:pointer;

}
.services_img_container{
  padding:1rem;
}

.services_btn{
  margin-top:2px;
  position:relative;
  bottom:20%;
  left:15%;
  background-color:black;
}
.paragraph{
  position:relative;
  bottom:30%;
  left:15%;
}
.work_header{
  margin:5rem;
  padding:5rem;
}
.work_para{
  font-size:1.2rem;
  max-width:40%;
}
.sect_container{
  background-color:#2F4858;
}
.padded{
  display:flex;
  flex-direction:row;
  align-items:center;
  justify-content:center;
}


</style>
