<template>
  <div id="app">
    <MyBottomVue></MyBottomVue>
    <MyHeadVue></MyHeadVue>
    <MyHomeVue></MyHomeVue>
    <MyAbout></MyAbout>
    <MyCounterTitleVue></MyCounterTitleVue>
    <MyCourseVue></MyCourseVue>
    <MyPricingVue></MyPricingVue>
    <MyJoinVue></MyJoinVue>
    <MyJoinDoubleVue></MyJoinDoubleVue>
    <MyShowVue></MyShowVue>
    <MymoreVue></MymoreVue>
    <MyTailVue></MyTailVue>
  </div>
</template>

<script>
import "./js/bootstrap4.js";
import "./js/bootstrap.bundle";
import MyBottomVue from "./components/MyBottom.vue";
import MyHeadVue from "./components/MyHead.vue";
import MyHomeVue from "./components/MyHome.vue";
import MyAbout from "./components/MyAboutTitle.vue";
import MyCounterTitleVue from "./components/MyCounterTitle.vue";
import MyCourseVue from "./components/MyCourse.vue";
import MyPricingVue from "./components/MyPricing.vue";
import MyJoinVue from "./components/MyJoin.vue";
import MyJoinDoubleVue from "./components/MyJoinDouble.vue";
import MyShowVue from "./components/MyShow.vue";
import MymoreVue from "./components/MyMore.vue";
import MyTailVue from "./components/MyTail.vue";
export default {
  name: "App",
  components: {
    MyBottomVue,
    MyHeadVue,
    MyHomeVue,
    MyAbout,
    MyCounterTitleVue,
    MyCourseVue,
    MyPricingVue,
    MyJoinVue,
    MyJoinDoubleVue,
    MyShowVue,
    MymoreVue,
    MyTailVue,
  },
  mounted() {
    let menu = document.querySelector("#menu-btn");
    let navbar = document.querySelector(".header .nav");

    menu.onclick = () => {
      menu.classList.toggle("fa-times");
      navbar.classList.toggle("active");
    };

    //头页导航
    window.onscroll = () => {
      menu.classList.remove("fa-times");
      navbar.classList.remove("active");

      if (window.scrollY > 0) {
        document.querySelector(".header").classList.add("active");
      } else {
        document.querySelector(".header").classList.remove("active");
      }
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css");
/* @import url('https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css'); */
@import "./css/bootstrap.css";
@import "./css/style.css";
@import "./css/mycss.css";
@import "./css/ltb.css";
@import "./css/font.css";
</style>

