<template>
  <div class="mask-layer" v-if="value">
    <div id="notice" class="notice-bg">
      <div class="notice-header">
        <img src="images/logo.png" width="250px">
        <span class="notice-close hand" @click="close">+</span>
      </div>
      <div class="notice-content">
        <p class="text-left">尊敬的会员：</p>
        <p class="text-justify text-indent">
          很高兴的通知您，为了给每一位忠诚玩家有更好的游戏体验和资金 保障，漫赢娱乐决定于2018年即日起与「亚太娱乐YT8.com」合并重 组，原漫赢娱乐所有玩家，将全部合并到「亚太娱乐YT8.com」，您可 使用原来的游戏账号登陆亚太娱乐并进行存款游戏，在此感谢每一位玩 家对本网站的支持。给您带来不便，敬请谅解。
        </p>
        <p class="text-justify text-indent">若有任何疑问，请及时联系在线客服或您的专属微信人员，进行咨 询，谢谢！</p>
        <p class="text-right">漫赢娱乐2018年3月10日</p>
        <div class="text-center">
          <button type="button" class="btn btn-secondary btn-notice">亚太娱乐登陆口</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "NoticeModal",
    props: {
      value: {
        type: Boolean
      }
    },
    methods: {
      close() {
        this.$emit("input", false);
      }
    }
  };
</script>

<style scoped>
  .mask-layer {
    background-color: rgba(0, 0, 0, 0.6);
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
  }

  .notice-bg {
    margin: 0 auto;
    text-align: center;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: #021439;
    height: 575px;
    width: 600px;
    padding: 10px;
    border-radius: 5px;
  }

  .notice-bg .notice-header {
    width: 210px;
    height: 42px;
    margin: 0 auto;
    position: relative;
  }

  .notice-bg .notice-header img {
    margin-top: 10px;
  }

  .notice-bg .notice-header .notice-close {
    position: absolute;
    right: -195px;
    top: -10px;
    font-size: 24px;
    -webkit-transform: rotate(45deg);
    transform: rotate(45deg);
    color: #fbd56f;
  }

  .notice-bg .notice-content {
    border-radius: 5px;
    margin-top: 10px;
    padding: 20px;
  }

  .notice-bg .notice-content p {
    color: #fff;
    line-height: 40px;
    font-size: 18px;
  }

  .notice-bg .button {
    width: 100%;
    padding: 1px 0;
    text-align: center;
    border-radius: 20px;
  }

  .text-left {
    text-align: left;
  }

  .text-right {
    text-align: right;
  }

  .text-justify {
    text-align: justify;
  }

  .text-indent {
    text-indent: 30px;
  }

  .btn-notice {
    border-radius: 5px;
    min-width: 220px;
    font-size: 18px;
    line-height: 32px;
    margin: 0 10px;
  }

  .btn-secondary {
    color: #000;
    background-color: #fbd56f;
    border-color: #fbd56f;
  }

  .text-center {
    text-align: center;
  }
</style>
