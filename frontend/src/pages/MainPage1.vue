<template>
    <div class="main">
      <div class="menu">
        <router-link to="/schedule" id="schedule">Расписание</router-link>
        <router-link to="/teams" id="teams">Сборные</router-link>
        <router-link to="/other" id="other">Другое</router-link>
        <router-link to="/l" id="profile" class="profile">Аккаунт</router-link>
      </div>
      <div class="navbar"></div>
      <div class="hover_green">
        <img class="hover_green2" src="../iconsMain/hover_green.svg">
      </div>
      <div class="hover_green_teams">
        <img  class="hover_green_teams2" src="../iconsMain/hover_green.svg">
    </div>
    <div class="hover_green_other">
        <img  class="hover_green_other2" src="../iconsMain/hover_green.svg">
    </div>
    <div class="hover_green_profile">
        <img  class="hover_green_profile2" src="../iconsMain/hover_green.svg">
    </div>
        <div class="leftContainer">
            <h1>Твой спорт!</h1>
            <div class="opisanieLinks">
                <p>Твой Спорт — площадка, которая поможет студентам 
                    и преподавателям отслеживать расписание тренировок
                    и соревнований, а также будет держать в курсе новостей спортивной жизни МГУ!</p>
                <ul>
                    <li>
                        <a href="">
                            <img src="../iconsMain/vk-gray 1.svg">
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <img src="../iconsMain/Telegram-2 1.svg">
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <img src="../iconsMain/email.svg">
                        </a>
                    </li>
                </ul>
            </div>
            <div class="balls">
                <div class="ball1">
                    <img src="../iconsMain/soccer.svg" alt="Soccer Ball">
                </div>
                <div class="ball2"></div>
            </div>
        </div>
        <div class="rightContainer">
            <div class="firstnews">
                <img src="../iconsMain/janosch-diggelmann-i8XiabUW3mw-unsplash 1.svg" class="beg">
                <div class="textfirst">
                    <h2>Спартакиада 2024</h2>
                    <p>Подробнее</p>
                </div>
            </div>
            
        </div>
        
      <div class="back">
        <div class="back0">
          <img class="img0" src="../iconsMain/gradient.svg">
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {

  }
  </script>
  
<style scoped>


* {
    overflow: hidden;
}

.main {
    width: 100%;
    position: absolute;
    display: flex;
    justify-content: space-between;
}
.back {
    width: 100%;
    position: absolute;
}
.back0 {
    position: absolute;
    margin-top: -13%;
    width: 100%;
    z-index: -1000;
    animation: gradient_anim 10s ease-in-out infinite;
}

a{
    color: black;
    text-decoration: none;;
}

.navbar {
    position: absolute;
    overflow: hidden;
    background-color: white;
    opacity: 0.5;
    width: 40%;
    height: 7%;
    z-index: 1;
    right: 0;
    margin-top: 0.6%;
    box-shadow: 1px 1px 8px 0.5px rgba(0, 0, 0, 0.09);
    margin-right: 3%;
}

.menu {
    position: absolute;
    z-index: 2;
    word-spacing: 2vw;
    display: inline-block;
    font-style: color black;
    text-align: center;
    width: 40%;
    height: 7%;
    font-size: 1.1vw;
    font-family: "Helvetica";
    margin-top: 1.6%;
    margin-left: 56%;
}

.profile {
    margin-left: 25%;
}

.sectionnone {
    display: none;
}

.sectionblock {
    display: block;
}

.hover_green2{
    position: absolute;
    margin-left: 23%;
    width: 30%;
    position: absolute;
    height: 0.2%;
    overflow: hidden;
    margin-top: -1%;
    box-shadow: 0px 16px 8px 22px #D5DF7C ;
    z-index: 1;
}

.hover_green_teams{
    position: absolute;
    margin-left: 62%;
    margin-top: 0.6%;
    width: 12%;
    height: 7%;
    overflow: hidden;
}

.hover_green_teams2{
    position: absolute;
    margin-left: 42%;
    width: 30%;
    position: absolute;
    height: 0.2%;
    overflow: hidden;
    margin-top: -1%;
    box-shadow: 0px 16px 8px 22px #D5DF7C ;
    z-index: 1;
}
.hover_green_other{
    position: absolute;
    margin-left: 68%;
    margin-top: 0.6%;
    width: 12%;
    height: 7%;
    overflow: hidden;
}

.hover_green_other2{
    position: absolute;
    margin-left: 47%;
    width: 30%;
    position: absolute;
    height: 0.2%;
    overflow: hidden;
    margin-top: -1%;
    box-shadow: 0px 16px 8px 22px #D5DF7C ;
    z-index: 1;
}
.hover_green_profile{
    position: absolute;
    margin-left: 86%;
    margin-top: 0.6%;
    width: 12%;
    height: 7%;
    overflow: hidden;
}

.hover_green_profile2{
    position: absolute;
    margin-left: 31%;
    width: 30%;
    position: absolute;
    height: 0.2%;
    overflow: hidden;
    margin-top: -1%;
    box-shadow: 0px 16px 8px 22px #D5DF7C ;
    z-index: 1;
}



ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
}

li {
    margin-right: 1vw; /* Adjust margin for better adaptation */
}

li:last-child {
    margin-right: 0;
}

.leftContainer {
    padding-left: 2vw;
    width: 45%;
    padding-top: 2%;
}

.leftContainer h1 {
    font-size: 7vw;
    font-family: "Helvetica";
    margin-bottom: 1%;
}

.leftContainer p {
    font-family: "Helvetica";
    font-size: 1.4vw;
}

.opisanieLinks {
    margin-left: 0.5vw;
    width: 80%;
}

.rightContainer {
    width: 55%;
    padding-top: 8%; 
}
.firstnews {
    display: block;
    margin-bottom: 2%; 
}

.textfirst {
    display: flex;
    justify-content: space-between;
    font-size: 1.4vw;
    margin-top: -2%; 
    align-items: center;
    width: 86%;
    font-family: "Helvetica";
    padding-left: 2%;
    box-shadow: 1px 1px 8px 0.5px rgba(0, 0, 0, 0.09);
}
.beg {
    width: 86%;
    padding-left: 2%;
}
.balls {
    position: absolute;
}

  </style>