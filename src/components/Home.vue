<template>

  
  <div class="background" :style="{'background-image': 'url(' + require('@/assets/background.jpg') + ')'}" >
    
  </div>


  <div class="container">
    <div class="Title">
      Andrew Marshall
    </div>

    <div class="Subtitle">Software Developer </div>
  </div>
  
  
  <div>
    <projects class="loadsecond"></projects>
  </div>

  <div class="btns">
    <a class="contact" href="">
      <div class="button">Contact Me</div>
    </a>
    <a class="about" href="">
      <div class="button">Resume</div>
    </a>
    <a class="github" href="">
      <div class="button">Github</div>
    </a>

  </div>
  
</template>

<script>
import projects from "./Project.vue"
export default {
  name: 'Home-Component',

  props: {
    msg: String
  },
  components:{
    projects
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.background{
  position: relative;
  height: fill;
  margin: 0;
  filter: blur(8px);
  -webkit-filter: blur(8px);

  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;

}

.container{
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0, 0); /* Black w/opacity/see-through */
  position: absolute;
  
  top: 20%;
  left:20%;

  transform: translate(-50%, -50%);

  filter: none;
  -webkit-filter: none;  
  animation: slideTopRight 5s;
}
.Title{
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0, 0); /* Black w/opacity/see-through */
  position: relative;
  
  top: 20%;
  left:20%;

  transform: translate(-50%, -50%);

  filter: none;
  -webkit-filter: none;

  font-size:  xx-large;
  
  
  animation: fadeIn 5s;

}

.Subtitle{
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0, 0); /* Black w/opacity/see-through */
  position: relative;

  font-size: x-large;
  opacity: 0%;
  top: 20%;
  left:20%;

  transform: translate(-50%, -50%);

  animation: fadeIn 5s;

  animation-delay: 5s;

  animation-fill-mode: forwards; 
}

.text{
  filter: none;
  -webkit-filter: none;
}

.loadsecond{

  opacity: 0%;
  animation-name: slideUp, fadeIn;
  animation-duration: 3s;
  animation-delay: 5s;
  animation-fill-mode: forwards; 
}

.contact{
  position:absolute;
  padding: 10px;
  top: 80%;

  float:left;
  
}
.about{
  position:absolute;
  padding: 10px;
  margin: left 20px;
  top: 80%;
}
.github{
  position:absolute;
  padding: 10px;
  margin: left 20px;
  top: 80%;
}

.button{
  background-color: rgba(102, 102, 102, 0.374);
  border-color: rgba(255, 255, 255, 0.112);
  padding: 4px;
  border-radius: 8px;
  border: 2px solid;


}
.btns{
  width:80%
}
@keyframes fadeIn {
  0% { opacity: 0; }
  100% { opacity: 1; }
  
}

@keyframes slideTopRight {
  0% {  left: 50%; top: 50%; }
  50% {  left: 50%; top: 50%;}
  99.9% {left: 20%; top: 20%; }
  100% {left: 20%; top: 20%; }
}

@keyframes slideUp{
  0% {transform: translateY(10px)}
  100% {transform: translateY(-10px)}
}


</style>
