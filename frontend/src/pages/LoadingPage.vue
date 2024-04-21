<template>

    <div class="page">
    <div class="back">
        <img class="back0" src="../iconsMain/gradient.svg"> 
    </div>
    <h1 class="welcome0">Добро пожаловать <br>в Твой Спорт!</h1>
    <div class="sport_decoration">
        <img class="basket1" src="../iconsballs/basket.svg">
        <img class="basket2" src="../iconsballs/basket.svg">
        <img class="volley1" src="../iconsballs/volley.svg">
        <img class="volley2" src="../iconsballs/volley.svg">
        <img class="regbi" src="../iconsballs/regbi.svg">
        <img class="volan" src="../iconsballs/volan.svg">
        <img class="tennis1" src="../iconsballs/tennis.svg">
        <img class="tennis2" src="../iconsballs/tennis.svg">
    </div>
</div>
  </template>
  
  <script>
import {useRouter} from 'vue-router'

const router = useRouter();
export default {
  created() {
    setTimeout(() => {
      this.$router.push({ path: '/main' });
    }, 2000); 
  }
}
  </script>
  
<style scoped>
@keyframes gradient_anim{
    0%{transform: scale(1);}
    50%{transform: scale(1.5);}
    100%{transform: scale(1);}
}

.page{
    overflow: hidden;
}

.h1{
    font-family: Helvetica;
}

.back{
    position: absolute;
    width: 100%;

}

.back0{
    position: absolute;
    margin-top: -13%;
    width: 100%;
    z-index: 0;
    animation: gradient_anim 10s ease-in-out infinite;
}
.welcome0{
  position: absolute;
  z-index: 10;
  font-size: 4.5vw;
  text-align: center;
  margin-top: 16%;
  margin-left: 30%;

}

.sport_decoration{
    position: absolute;
    width: 100%;
}

.basket1{
    position: absolute;
    margin-top: -130%;
    margin-left: -195%;
    width: 120%;
    rotate: -120deg;
}
.basket2{
    position: absolute;
    width: 45%;
    margin-top: -75%;
    margin-left: 52%;
    rotate: 10deg;
}

.volley1{
    position: absolute;
    width: 120%;
    rotate: -120deg;
    margin-left: 66%;
    margin-top: -10%;
}

.volley2{
    position: absolute;
    width: 45%;
    margin-left: -110%;
    margin-top: -2%;
    
}

.regbi{
    margin-top: 5%;
    position: absolute;
    width: 35%;
    margin-left: 4%;
}

.volan{
    position: absolute;
    width: 20%;
    margin-top: -70%;
    margin-left: -30%;
}

.tennis1{
    position: absolute;
    width: 13%;
    margin-left: 90%;
    margin-top: -30%;
}

.tennis2{
    position: absolute;
    width: 13%;
    margin-left: -90%;
    margin-top: -25%;
    rotate: -30deg;
}





</style>