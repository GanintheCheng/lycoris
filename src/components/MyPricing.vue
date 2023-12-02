<template>
  <section class="pricing" id="pricing">
    <div class="heading">
      <span>官图轮播</span>
      <h3>OFFICIAL MAP ROTATION</h3>
    </div>
    <div class="lunbotu">
      <div class="baodi">
        <div class="LBT">
          <div id="slide">
            <div
              class="item"
              :style="{
                backgroundImage: 'url(' + require('../img/takina08.png') + ')',
              }"
            >
              <div class="lhx">
                <div class="name">莉可丽丝</div>
                <div class="des">Lycoris Recoil</div>
              </div>
            </div>
            <div
              class="item"
              :style="{
                backgroundImage: 'url(' + require('../img/tc09.png') + ')',
              }"
            >
              <div class="lhx">
                <div class="name">莉可丽丝</div>
                <div class="des">Lycoris Recoil</div>
              </div>
            </div>
            <div
              class="item"
              :style="{
                backgroundImage: 'url(' + require('../img/tc03.png') + ')',
              }"
            >
              <div class="lhx">
                <div class="name">莉可丽丝</div>
                <div class="des">Lycoris Recoil</div>
              </div>
            </div>
            <div
              class="item"
              :style="{
                backgroundImage: 'url(' + require('../img/tc10.png') + ')',
              }"
            >
              <div class="lhx">
                <div class="name">莉可丽丝</div>
                <div class="des">Lycoris Recoil</div>
              </div>
            </div>
            <div
              class="item"
              :style="{
                backgroundImage: 'url(' + require('../img/tc05.png') + ')',
              }"
            >
              <div class="lhx">
                <div class="name">莉可丽丝</div>
                <div class="des">Lycoris Recoil</div>
              </div>
            </div>
            <div
              class="item"
              :style="{
                backgroundImage: 'url(' + require('../img/ly05.png') + ')',
              }"
            >
              <div class="lhx">
                <div class="name">莉可丽丝</div>
                <div class="des">Lycoris Recoil</div>
              </div>
            </div>
          </div>
          <div class="buttons">
            <div class="s_button">&lt;</div>
            <div class="s_button">&gt;</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    //官图轮播图
    let direction = true;

    let move = () => {
      let lists = document.querySelectorAll(".item");
      if (direction) {
        document.querySelector("#slide").appendChild(lists[0]);
      } else {
        document.querySelector("#slide").prepend(lists[lists.length - 1]);
      }
    };

    this.timer = setInterval(move, 2500);

    document.querySelector(".LBT").addEventListener("mouseover", () => {
      clearInterval(this.timer);
    });

    document.querySelector(".LBT").addEventListener("mouseout", () => {
      this.timer = setInterval(move, 2500);
    });

    document.querySelectorAll(".s_button")[1].onclick = () => {
      direction = true;
      move();
      console.log("向右");
    };

    document.querySelectorAll(".s_button")[0].onclick = () => {
      direction = false;
      move();
      console.log("向左");
    };
  },
};
</script>

<style>
</style>