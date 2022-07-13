<script>
export default{
  data(){
    return{
      navItems:['ABOUT', 'PROGRAMS', 'DONATE', 'VOLUNTEER ', 'EVENTS'],
      apply:['Apply', 'Donate', 'Volunteer']

    }
  },
   created(){
    
   }  
}
</script>

<template>
<center>
  <div style="width:100%; height:65px; background-color:black; position:fixed"><li id="topBar" v-for="app in apply" :key="app" style="position:relative; left:35%;  ">{{app}}</li></div>

<div id ="logo" style=" width:60%; height: 150px; disply:grid">
<img v-bind:src="'src/assets/logoDog3.png'" style="z-index:1; float:left; width:250px; height:250px; position:relative; right:-90px; top:40px;"/>
<div style="height:300px; width:100%; background-color:transparent">
<h1 style="color:#911010; font-size:60px; position:relative; top:80px;
left:30px;">NOVA THE WONDER DOG</h1>

  <div style="position:relative; top:70px; left:10px;">
<li id="navBar" v-for="item in navItems" :key="item">
  {{item}}
  </li>
  <hr/>
  </div>
</div>
  </div>
</center>



</template>

<style>
*{
  margin:0;
  padding:0;
}
li{
  display: inline-block;
  z-index:2;
  color:black;
  font-size: 20px;
  padding:20px;
}
#topBar{
  color:#911010;
  cursor: pointer;
}
#topBar:hover{
  border:2px solid #911010
}

#navBar:hover{
  background-color: black;
  color:#911010;
  cursor: pointer;
}
hr{
  position: relative;
  height:50px;
  border:0px;
  width:61%;
   background: url(src/assets/star.png);
  bottom:10px;
}
#app {
  padding:0;
  margin:0;
background: url(src/assets/back.png);
background-size: cover;
background-repeat: no-repeat;
height:1200px;
position: absolute;
width:100%;
z-index: 0;
  box-sizing: border-box;

}
</style>
