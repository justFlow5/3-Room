<template>
  <div class="doodles-container">
    <vue-css-doodle>
      :doodle { @grid: 20 / 100vmax; grid-gap: 4vmax; } background: #26C6DA;
      transform: scale(@rand(.1, .9)) translate3d(@r(50px), @r(100px), 0);
      background: hsla(@r(360), 85%, @r(70%, 90%), @r(.9)); border-radius:
      @r(10px);
    </vue-css-doodle>
    <img src="../../../assets/doodles/3-leaves.png" alt="3 leaves" />
    <img src="../../../assets/doodles/fatarrow.png" alt="fat arrow" />
    <img
      src="../../../assets/doodles/cross.png"
      alt="cross"
      :class="{ show: isMenuOpen }"
    />
    <img src="../../../assets/doodles/notebook.png" alt="notebook" />
    <img src="../../../assets/doodles/pencil.png" alt="pencil" />
    <img src="../../../assets/doodles/ruler.png" alt="ruler" />
    <img src="../../../assets/doodles/thinarrow.png" alt="thin arrow" />
    <img src="../../../assets/doodles/coffee.png" alt="coffee cup" />
    <img src="../../../assets/doodles/pen.png" alt="pen" />
  </div>
</template>

<script>
export default {
  name: 'RandomDoodles',
  props: ['isMenuOpen'],
};
</script>

<style lang="scss" scoped>
.doodles-container {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 0;
  & > img {
    position: absolute;
    transition: all 0.6s 0.4s;
    opacity: 0.8;
    width: 40px;
    height: 40px;

    @media (min-width: $mobileL) {
      width: 55px;
      height: 55px;
      &.show {
        opacity: 0 !important;
        transition: all 0.3s;
      }
    }

    @media (min-width: $tablet) {
      width: 100px;
      height: 100px;
    }

    @media (min-width: $laptopL) {
      width: 120px;
      height: 120px;
    }

    @media (min-width: $desktop) {
      width: 140px;
      height: 140px;
    }

    &:nth-child(1) {
      top: 1%;
      left: 10%;

      @media (min-width: $tablet) {
        top: 3%;
        left: 2%;
      }
    }

    &:nth-child(2) {
      left: 40%;
      top: 2%;
      @media (min-width: $tablet) {
        left: unset;
        top: 7%;
        right: 6%;
      }
    }
    &:nth-child(3) {
      top: 25%;
      right: 6%;

      @media (min-width: $mobileL) {
        top: 34%;
        right: 13%;
      }
    }
    &:nth-child(4) {
      top: 40%;
      right: 3%;
      opacity: 0.6;

      @media (min-width: $mobileL) {
        top: unset;
        opacity: 0.8;
        bottom: 7%;
        right: 10%;
      }
    }
    &:nth-child(5) {
      bottom: 6%;
      right: 40%;
      @media (min-width: $mobileL) {
        bottom: 30%;
        left: 1%;
        right: unset;
      }
    }
    &:nth-child(6) {
      bottom: 2%;
      right: 72%;

      @media (min-width: $mobileL) {
        bottom: 30%;
        right: 2%;
      }
    }
    &:nth-child(7) {
      bottom: 11%;
      left: 10%;
    }
    &:nth-child(8) {
      bottom: 7%;
      left: 30%;
      opacity: 0.6;
      width: 30px;
      height: 30px;

      @media (min-width: $tablet) {
        opacity: 0.8;
        bottom: unset;
        top: 40%;
        left: 16%;
        width: 50px;
        height: 50px;
      }
    }
    &:nth-child(9) {
      top: 19%;
      left: 4%;
      width: 50px;
      height: 50px;
      opacity: 0.5;
      @media (min-width: $tablet) {
        opacity: 0.8;
        top: 27%;
        left: 6%;
        width: 80px;
        height: 80px;
      }
    }

    &:nth-child(10) {
      left: 10%;
      top: 0;
      @media (min-width: $tablet) {
        left: 4%;
      }
    }
  }
}
</style>
