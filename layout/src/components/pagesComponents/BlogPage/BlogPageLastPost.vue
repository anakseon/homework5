<template>
  <section class="latest-post center">
    <h2 class="latest-post__title">Последний пост</h2>
    <div class="latest-post__wrap">
      <img src="../../../assets/images/latest-post-img.jpg" alt="latest-post-img" class="latest-post__img">
      <div class="latest-post__content">
        <h3 class="latest-post__content-title">Low Cost Latest Invented Interior Designing Ideas</h3>
        <p class="latest-post__content-text">С того времени этот, похожий на латинский, текст стал стандартом в печатной промышленности для примеров шрифтов и текстов. Перед появлением электронных издательств дизайнеры импровизировали в работе над макетами, изображая текст при помощи волнистых линий. С появлением самоклеющихся наклеек с напечатанным текстом «Lorem ipsum» появился более реалистичный способ обозначения расположения текста на странице.</p>
        <div class="latest-post__content-wrap">
          <p class="latest-post__content-data">26 декабря, 2022</p>
          <a href="#">
            <img src="../../../assets/images/row_left_blog.svg" alt="row_left_blog">
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'BlogPageLastPost',

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

.latest-post {
  &__title {
    margin-top: 200px;
    margin-bottom: 27px;
    color: #292f36;
    font-family: $familyTitle;
    font-size: 50px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    /* 62.5px */
    letter-spacing: 1px;
  }

  &__wrap {
    border: 1px solid #e7e7e7;
    display: flex;
    gap: 62px;
    padding: 22px;
    border-radius: 62px;
    align-items: center;
  }

  &__img {
    border-radius: 50px;
  }

  &__content {
    width: 489px;

    &-title {
      margin-bottom: 22px;
      color: #292f36;
      font-family: $familyTitle;
      font-size: 25px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
      letter-spacing: 0.5px;
    }

    &-text {
      margin-bottom: 41px;
      color: #4d5053;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
    }

    &-wrap {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: nowrap;
    }

    &-data {
      color: #4d5053;
      font-family: $familyText;
      font-size: 16px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.16px;
      text-transform: capitalize;
    }
  }
}
</style>
