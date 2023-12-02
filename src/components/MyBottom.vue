<template>
  <section class="bottom">
    <div class="text"></div>
    <img src="@/img/tc02.png" alt="" />
  </section>
</template>

<script>
export default {
  mounted() {
    let text = document.querySelector(".bottom .text");
    let img = document.querySelector(".bottom img");
    let count = -1,
      timeout = 0;
    let textamount = ["黑色的那位是泷奈", "千束是红色的那位"];
    img.addEventListener("click", () => {
      if (++count > 1) count = 0;
      text.innerHTML = textamount[count];
      text.classList.add("active");
      if (count == 0) {
        text.style.color = "black";
      } else {
        text.style.color = "red";
      }
      clearTimeout(timeout);
      timeout = setTimeout(() => {
        text.classList.remove("active");
      }, 2000);
    });
  },
};
</script>

<style>
</style>