<template>
  <div class="container-flower">
    <div class="row">
      <div class="col p-4">
        <img
          alt="horizontal"
          src="../assets/sm_hrizontal_2.svg"
          class="item-img"
        />
      </div>
    </div>
    <div class="row m-4 show-time">{{ getShowHour }}</div>
    <div class="row m-4 title-text">COMOMING SOON</div>
    <div class="row p-0 position-relative">
      <div class="col">
        <img alt="shild" src="../assets/shild.png" class="bottom-100 end-100" />
      </div>
    </div>
    <div class="row position-relative">
      <div class="col">
        <img
          alt="nombre"
          src="../assets/flower_girl.svg"
          class="position-absolute bottom-100 end-0"
        />
      </div>
    </div>
    <div class="row ">
      <div class="d-grid gap-2 d-md-block position-absolute top-100 end-0">
        <button class="btn btn-link btn-sm" type="button"><img src="../assets/instagram.png" alt=""></button>
        <button class="btn btn-link btn-sm" type="button"><img src="../assets/facebook.png" alt=""></button>
        <button class="btn btn-link btn-sm" type="button"><img src="../assets/telegram.png" alt=""></button>
        <button class="btn btn-link btn-sm" type="button"><img src="../assets/play.png" alt=""></button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hour: 0,
      minutes: 0,
      seconds: 0,
    };
  },
  created() {
    setInterval(() => this.updateHour(), 1000);
  },
  methods: {
    updateHour() {
      let date = new Date();
      this.hour = date.getHours();
      this.minutes = date.getMinutes();
      this.seconds = date.getSeconds();

      this.minutes =
        this.minutes > 9 ? this.minutes : "0" + this.minutes.toString();
      this.seconds =
        this.seconds > 9 ? this.seconds : "0" + this.seconds.toString();
    },
  },
  computed: {
    getShowHour() {
      return `${this.hour}:${this.minutes}:${this.seconds}`;
    },
  },
};
</script>

<style>
.container-flower {
  position: relative;
  width: 360px;
  height: 640px;
  background: #8439e9;
  padding: 10px 10px 40px 30px;
}
.show-time {
  left: 8.06%;
  right: 50%;
  top: 19.38%;
  bottom: 78.12%;

  font-family: DINPro;
  font-style: normal;
  font-weight: bold;
  font-size: 18px;
  line-height: 105.8%;
  /* or 19px */

  color: #ffffff;
}
.title-text {
  left: 8.06%;
  right: 37.78%;
  top: 22.66%;
  bottom: 66.25%;

  font-family: DINPro;
  font-style: normal;
  font-weight: bold;
  font-size: 36px;
  line-height: 105.8%;
  /* or 38px */

  color: #fdbc1b;
}
</style>
