<template>
  
    <div class="projectscontainer">
    
        <div class="text">
            My Projects:
        </div>
        <div class="text" :style="{'font-weight':'bold'}">
            Leviathan Engine
        </div>
        <a href="https://www.github.com/afk47/leviathan-engine">
            <div class="image" :style="{'background-image': 'url(' + require('@/assets/Leviathan.png') + ')'}">

            </div>
            <div class="projdescription"> 
                C++ Game Engine/Framework. Utilizes OpenGL with plans to implement DirectX and Vulkan in the future.
                Early in development.
            </div>
        </a>
         

    </div>
    
    
    
</template> 
  
  <script>
  export default { 
    name: 'ProjectsView',
    
  }
  </script>
  
<style>
  
  .projectscontainer{
    background-color: rgb(0, 0, 0, 0.3);

    border-color: rgba(1, 1, 1, 1);

    border-radius: 8px;
    border: 2px solid;
    position:   absolute;
    right:  5%;
    top: 20%;

    width: 30%;
    height: 70%;
    
    margin: auto;
  }

  .image{
    float: left;
    margin:auto;
    margin-left: 5%;
    padding:10%;
    background-size: contain;
    background-repeat: no-repeat;
  }

  .projdescription{
    float: right;
    padding:5%;
    font-size: small;
    width: 65%;
    height: fit-content;
    position: relative;
  }

  .text{
    padding:2%;
  }

  a{
    color: white;
    font-weight: normal;
    text-decoration: none;
  }
  </style>
  