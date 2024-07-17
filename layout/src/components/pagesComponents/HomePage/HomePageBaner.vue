<template>
   <section class="baner center">
      <div class="baner__wrap">
         <div class="baner__wrap-content">
            <h1 class="baner__title">Пусть ваш дом будет уникальным</h1>
            <p class="baner__text">Существует много вариаций Lorem Ipsum, которые можно использовать</p>
            <a href="#" class="baner__button">
               <div class="baner__button-text">
                  <p>Начать</p>
                  <img src="../../../assets/images/row_left.svg" alt="row_left">
               </div>
            </a>
         </div>
      </div>
   </section>
</template>

<script>
export default {
  name: 'HomePageBaner',

  data () {
    return {

    }
  },

  mounted () {

  },

  methods: {

  }
}
</script>

<style lang="scss" scoped>
@import "../../../scss/vars";
.baner {
   &__wrap {
      height: 758px;
      background-image: url("../../../assets/images/Header_Photo.jpg");
      background-repeat: no-repeat;
      border-radius: 75px;
   }
   &__wrap-content {
      padding: 208px 715px 0 52px;
   }
   &__title {
      margin-bottom: 18px;
      color: #292f36;
      font-family: $familyTitle;
      font-size: 65px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
   }
   &__text {
      color: #4d5053;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
      margin-bottom: 21px;
   }
   &__button-text {
      width: 220px;
      padding: 26px 0;
      background-color: #292f36;
      border-radius: 18px;
      display: flex;
      gap: 10px;
      flex-direction: row;
      flex-wrap: nowrap;
      justify-content: center;
      align-items: center;
      & p {
         color: #fff;
         font-family: $familyText;
         font-size: 18px;
         font-style: normal;
         font-weight: 600;
         line-height: 125%;
         letter-spacing: 0.36px;
      }
   }
}
</style>
