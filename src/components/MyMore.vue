<template>
  <section class="more" id="more">
    <div class="head">
      <span>了解更多</span>
      <h3>learn about more</h3>
    </div>
    <div class="container">
      <h2 style="margin-left: 2px">各话剧情</h2>
      <div class="row row-cols-13" ref="row">
        <div class="col" v-for="(item, index) in 13" :key="index">
          <button :value="index + 1">{{ index + 1 }}</button>
        </div>
      </div>
      <div class="thing">
        <h1 style="text-align: center">选择集数查看剧情</h1>
        <span class="span">......</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      len: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13],
    };
  },
  mounted() {
    let progress = [
      "",
      "身为维护日本治安的秘密特工“Lycoris”的井之上泷奈，因为某个事件被调职到咖啡店“LycoReco”。泷奈与超优秀的No.1Lycoris（？）千束组成搭档，干劲十足地以尽快重返DA总部为目标。然而，LycoReco的工作却非常特别！？",
      "顶级黑客Walnut向LycoReco发出了求救！Walnut称其他黑客想要她的性命，希望能帮助她逃往国外。LycoReco的成员齐心协力帮助Walnut逃跑，但千束等人却遭到了严密的武装集团的袭击……！？",
      `为了进行身体检查和体能测试，千束不情愿地前往DA总部。听闻这件事的泷奈，为了找司令谈判回归DA，也决定要一起过去。虽然千束也帮忙交涉，可司令根本不听她们的话而且，自己原来的搭档风希已经有了新搭档……`,
      `DA总部的那件事后，千束和泷奈在LycoReco过着顺利的生活。某日，千束发现泷奈的内裤居然是■■■■■■……看到泷奈对自己的事这么不上心，大吃一惊的千束决定带她出门购物！`,
      `延空木的事件也告一段落了——正当千束这么想的时候，在旧电波塔被打倒的真岛，再次出现在千束面前！！！在延空木放置炸弹的真岛，以爆破为赌注，与千束展开一对一的对决。千束的时限也快到了，最终之战就此打响。`,
      `接连发生Lycoris遭到袭击的事件。为避免单独行动，泷奈决定住在千束家。但是，第一次的二人生活尽是些意料之外的事情！？另一方面，一直在秘密探查DA拥有的情报的胡桃，迫近了Lycoris袭击事件的意外真相——`,
      `米卡收到了一封短信。碰巧看到这封短信的千束，怀疑楠木想把自己带回DA！她胡思乱想，吵闹着得出了LycoReco要倒闭的暴论。为了阻止计划，Lycoris的四人齐心协力，瞒着米卡突击约定地点的酒吧！`,
      `米卡收到了一封短信。碰巧看到这封短信的千束，怀疑楠木想把自己带回DA！她胡思乱想，吵闹着得出了LycoReco要倒闭的暴论。为了阻止计划，Lycoris的四人齐心协力，瞒着米卡突击约定地点的酒吧！`,
      `千束的人造心脏被盯上了。由于电池无法再充电，千束被宣告时日无多。追查无法替代的人造心脏的线索的胡桃，向米卡询问了当时的事情。另一方面，DA在采取大规模的真岛讨伐作战前，把千束叫到了本部。`,
      `千束为了不让瑞希和胡桃被自己的事情束缚，决定闭店。与此同时，回到DA的泷奈为了拯救千束的命，打算以真岛为线索追查吉松的行踪。她终于捕获了真岛的委托人，潜入了据点，但......？`,
      `为了阻止真岛，DA的Lycoris准备进入延空木。在执行作战之前，泷奈从楠木那里听说无法联系到千束，于是急忙单独赶往咖啡店。然而，收到机器太威胁的千束和米卡，选择前往旧电波塔解救吉松。`,
      `千束在旧电波塔与真岛陷入苦战，泷奈在千钧一发之际赶到。另一边，由于真岛的策略，Lycoris的存在向世人公开了。在本部，高层宣布剥夺楠木司令的指挥权，并决定处分在延空木的风希等Lycoris……？！`,
      `延空木的事件也告一段落了——正当千束这么想的时候，在旧电波塔被打倒的真岛，再次出现在千束面前！！！在延空木放置炸弹的真岛，以爆破为赌注，与千束展开一对一的对决。千束的时限也快到了，最终之战就此打响。`,
    ];
    let title = [
      ``,
      `慢慢来`,
      `多多益善`,
      `欲速则不达`,
      `无所求则无所获`,
      `目前为止，一切顺利`,
      `相斥相吸`,
      `时间会证明一切`,
      `又一日，又一文`,
      `覆水难收`,
      `以恶报恶`,
      `棋逢对手`,
      `先天与后天`,
      `Recoil of Lycoris`,
    ];
    this.$refs.row.addEventListener("click", (e) => {
      if (e.target.tagName == "BUTTON") {
        // console.log(e.target.value);
        document.querySelector(`.more .thing h1`).innerHTML =
          title[e.target.value];
        document.querySelector(`.more .thing span`).innerHTML =
          progress[e.target.value];
      }
    });
  },
};
</script>

<style>
</style>