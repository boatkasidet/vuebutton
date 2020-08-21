<template>
 <div id="app">
    <HelloWorld msg />
    <hr>
    <div class="row">
      <div class="col-6">
        <img src="https://scontent.fcnx4-1.fna.fbcdn.net/v/t1.0-9/115805540_1958216880980271_1509939533218489563_o.jpg?_nc_cat=109&_nc_sid=09cbfe&_nc_eui2=AeEVOjuaFyz2sF0ectidLgT7nfB3aJ5ENFGd8HdonkQ0UZXR0yRZ6gfDAPPLKjpgIg3BHF2Im4jnFUSC6tpR7dgL&_nc_ohc=XTVApjxu_qEAX_4T5ps&_nc_oc=AQl_FDZXGWwjbYYjHgmrTx8ce_0xUg7iRYoxjA_R-LEkUOdzFHnP0iIWaZ2RaO0mzgnDxLXaYPwuwGJdA2UhVuiU&_nc_ht=scontent.fcnx4-1.fna&oh=7d497cddc51942f1c57cbd8247c2e738&oe=5F655E8E" width="300" height="300" />
        <h1>{{total1}}</h1>
      </div>
      <div class="col-6">
        <img src="https://scontent.fcnx4-1.fna.fbcdn.net/v/t1.0-9/78754519_1719211401547488_8245157574077317120_o.jpg?_nc_cat=111&_nc_sid=174925&_nc_eui2=AeHiPVoeiC6f9OFN-25KuCscZcQMKcXfMCBlxAwpxd8wIPr9I9a_5U_TkCHhLfhcf4_a36kc-Asb8f7JPSZ7ICLR&_nc_ohc=Ypxd46CCQyIAX_tAMMT&_nc_ht=scontent.fcnx4-1.fna&oh=d986584148eefa55aa2e495e3aa51c09&oe=5F648A64" width="300" height="300" />
        <h1>{{total2}}</h1>
      </div>
      <div class="col-6">
        <CsButton @cc="sum" />
      </div>
      <div class="col-6">
        <CsButton @cc="sum1" />
      </div>
    </div>
    
  </div>
</template>
<script>
import HelloWorld from "./components/HelloWorld.vue";
import CsButton from "./components/CSButton.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    CsButton,
    
  },
  data : function(){
    return {
    total1: 0,
    total2: 0,
   
   } 
  },
  methods: {
  sum(counterValue){
    this.total1 = counterValue
  },
  
  sum1(counterValue){
    this.total2 = counterValue
 
  
},
},

};

</script>

<style>

body{
  background-image: url(https://wallpaperaccess.com/full/7285.jpg);
  background-size: 100%;
}

#app {
  
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color:black;
  margin-top: 60px;
}
</style>