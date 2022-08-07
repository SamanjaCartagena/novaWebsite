<script>
import image from './assets/logo.png'
import carousalimage1 from './assets/pic2.jpg'
import carousalimage2 from './assets/image1.jpg'
import carousalimage3 from './assets/image2.jpg'
import carousalimage4 from './assets/image9.jpg'
import carousalimage5 from './assets/image6.jpg'
import carousalimage6 from './assets/image7.jpg'
import carousalimage7 from './assets/pic2.jpg'
import arizona from './assets/arizona.jpg'

export default{
  data(){
    return{
      navItems:['ABOUT', 'PROGRAMS', 'DONATE', 'VOLUNTEER ', 'EVENTS'],
      apply:['Apply', 'Donate', 'Volunteer'],
      logo:image,
      arizona:arizona,
     carousal:[
        carousalimage1,carousalimage2,carousalimage3,carousalimage4,carousalimage5,carousalimage6
     ]

    }
  },
   created(){
    
   }  
}
</script>

<template>
   
<center>
  <div style="width:100%; height:65px; background-color:black; position:fixed">
    <li id="topBar" v-for="app in apply" :key="app" style="position:relative; left:35%;  ">{{app}}</li>
    </div>

<div id ="logo" >
<img :src="this.logo" style="float:left; position:relative; bottom:50px;right:200px; width:auto;" />

<div style="height:300px; width:100%; background-color:transparent">

 <center>
  <div style="position:relative;top:150px;right:25%">
    <h1 style="fontSize:50px">K9 Paws Behavior Dog Training</h1>
<li id="navBar" v-for="item in navItems" :key="item">
  {{item}}
  </li>
  <hr style="border:1px solid black;"/>
  </div>
 </center>
</div>
<div style="position:relative; top:50px">
 <el-carousel :interval="4000" type="card" height="700px">
    <el-carousel-item v-for="item in carousal" :key="item">
<img :src="item" style="height:700px;" />
    </el-carousel-item>
  </el-carousel>
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
  font-size: 17px;
  padding:20px;
}

#topBar{
  color:#95b7d0;
  cursor: pointer;
}
#topBar:hover{
  border:2px solid #95b7d0;
  font-size: 25px;
 
}

#navBar:hover{
  background-color: black;
  color:#95b7d0;
  cursor: pointer;
}

#app {
  padding:0;
  margin:0;
background: url(assets/arizona.jpg);
background-size: cover;
background-repeat: no-repeat;
height:1200px;
position: absolute;
width:100%;
z-index: 0;
  box-sizing: border-box;

}
.el-carousel__item h3 {
  color: #475669;
  opacity:1;
  line-height: 200px;
  margin: 0;
  text-align: center;
}

.el-carousel__item:nth-child(2n) {
  background-color: transparent;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: transparent;
}
</style>
