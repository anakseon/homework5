<template>
  <section class="blog-details-page center">
    <div class="blog-details__wrap">
      <div class="blog-details">
        <div class="article" v-for="article in filterArticle" :key="article.id">
          <h2 class="article__title">{{ article.title }}</h2>
          <img class="article__img" :src="require('../../../assets/images/' + article.img)" :alt="article.img">
          <div class="article__info">
            <p class="article__info-data">26 декабря,2022</p>
            <p class="article__info-link">Интерьер / Домой / Декор</p>
          </div>
          <p class="article__text">В своей статье от 1994-го года журнал «Before & After» отследил фразу «Lorem ipsum ...» до философского трактата Цицерона О пределах добра и зла, написанного в 45 году до нашей эры на латинском языке.</p>
          <br>
          <p class="article__text">В оригинале текст выглядит так «Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit ...», и переводится как «Нет никого, кто любил бы свою боль, кто искал бы ее и хотел бы чтобы она была у него. Потому что это боль...»</p>
          <div class="info-blok">
            <p class="info-blok__quotation-marks">&#8221;</p>
            <p class="info-blok__text">Какая-то умная и красивая цитата</p>
          </div>
          <h2 class="article__title">Design sprints are great</h2>
          <p class="article__text"> В оригинале текст выглядит так «Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit ...», и переводится как «Нет никого, кто любил бы свою боль, кто искал бы ее и хотел бы чтобы она была у него. Потому что это боль...» </p>
          <div class="article__list">
            <div class="article__list-num">
              <p class="article__list-num-text">1</p>
              <p class="article__list-item">С того времени этот, похожий на латинский, текст стал стандартом в печатной промышленности для примеров шрифтов и текстов.</p>
            </div>
            <div class="article__list-num">
              <p class="article__list-num-text">2</p>
              <p class="article__list-item">С того времени этот, похожий на латинский, текст стал стандартом в печатной промышленности для примеров шрифтов и текстов.</p>
            </div>
            <div class="article__list-num">
              <p class="article__list-num-text">3</p>
              <p class="article__list-item">С того времени этот, похожий на латинский, текст стал стандартом в печатной промышленности для примеров шрифтов и текстов.</p>
            </div>
          </div>
          <img class="article__img" src="../../../assets/images/article_1_1.jpg" alt="article 1_1">
          <p class="article__text">В своей статье от 1994-го года журнал «Before & After» отследил фразу «Lorem ipsum ...» до философского трактата Цицерона О пределах добра и зла, написанного в 45 году до нашей эры на латинском языке.</p>
        </div>
      </div>
      <div class="tags">
        <div class="tags__buttons-wrap">
          <h2 class="tags__title">Тэги</h2>
          <div class="tags__buttons">
            <button v-for="(btn, index) in buttonList" @click="filterClick(btn)" class="tags__buttons-item"
              :key="index">{{ btn }}</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'BlogDetailsPageArticles',

  data () {
    return {
      findelement: '',
      contentsArticles: [
        {
          id: 0,
          title: 'Создадим лучший макет перепланировки',
          img: 'article_1.jpg',
          tag: 'Кухня'
        },
        {
          id: 1,
          title: 'Лучшие интерьерные идеи по низкой цене',
          img: 'image_2.jpg',
          tag: 'Спальня'
        },
        {
          id: 2,
          title: 'Лучшие интерьерные решения для офисов',
          img: 'image_3.jpg',
          tag: 'Здание'
        },
        {
          id: 3,
          title: 'Low Cost Latest Invented Interior Designing Ideas.',
          img: 'image_4.jpg',
          tag: 'Архитектура'
        },
        {
          id: 4,
          title: 'Лучшие интерьерные решения для офисов',
          img: 'image_4.jpg',
          tag: 'Планировка'
        }
      ],
      buttonList: [
        "Кухня",
        "Спальня",
        "Здание",
        "Архитектура",
        "Планировка",
        "Спальня",
      ]
    }
  },

  mounted () {

  },

  methods: {
    filterClick (item) {
      this.findelement = item
    }
  },
  computed: {
    filterArticle () {
      return this.findelement
        ? this.contentsArticles.filter((el) => el.tag.includes(this.findelement))
        : this.contentsArticles
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../../../scss/vars";

.blog-details__wrap {
  margin-top: 200px;
  display: flex;
  gap: 52px;
}

.blog-details {
  width: 800px;
}

.article {
  margin-bottom: 96px;

  &__title {
    color: #292f36;
    font-family: $familyTitle;
    font-size: 50px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    letter-spacing: 1px;
    margin-bottom: 20px;
  }

  &__img {
    margin-top: 21px;
    margin-bottom: 35px;
    border-radius: 50px;
  }

  &__info {
    margin-top: 11px;
    display: flex;
    justify-content: space-between;
    margin-bottom: 46px;
    color: #4d5053;
    font-family: $familyText;
    font-size: 16px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 150%;
    letter-spacing: 0.16px;
    text-transform: capitalize;
  }

  &__text {
    color: #4d5053;
    font-family: $familyText;
    font-size: 22px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 150%;
    letter-spacing: 0.22px;
  }

  &__list {
    margin-top: 24px;
    margin-bottom: 23px;
    display: flex;
    width: 732.389px;
    flex-direction: column;
    align-items: flex-start;
    gap: 32px;
    list-style-position: 10px 0;

    &-num {
      display: flex;
      align-items: flex-start;
      gap: 14px;

      &-text {
        color: #cda274;
        font-family: $familyTitle;
        font-size: 20px;
        font-style: normal;
        font-weight: $font-400;
        line-height: 125%;
        letter-spacing: 0.4px;
      }
    }

    &-item {
      color: #4d5053;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
    }
  }
}

.tags {
  &__buttons-wrap {
    width: 345px;
    display: flex;
    flex-direction: column;
    gap: 24px;
  }

  &__title {
    color: #292f36;
    font-family: $familyTitle;
    font-size: 25px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    letter-spacing: 0.5px;
  }

  &__buttons {
    display: grid;
    grid-template-columns: repeat(2, auto);
    gap: 10px;

    &-item {
      cursor: pointer;
      background: #f4f0ec;
      padding-top: 9px;
      padding-bottom: 9px;
      border-radius: 10px;
      border: none;
      color: #292f36;
      text-align: center;
      font-family: $familyText;
      font-size: 18px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
      letter-spacing: 0.36px;
    }
  }
}

.info-blok {
  margin-bottom: 27px;
  margin-top: 35px;
  padding: 53px 227px;
  background: #f4f0ec;
  border-radius: 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;

  &__quotation-marks {
    width: 106px;
    height: 133px;
    flex-shrink: 0;
    color: #cda274;
    text-align: center;
    font-family: $familyTitle;
    font-size: 200px;
    font-style: italic;
    font-weight: $font-400;
    line-height: 125%;
    letter-spacing: 4px;
  }

  &__text {
    color: #cda274;
    text-align: center;
    font-family: $familyTitle;
    font-size: 25px;
    font-style: italic;
    font-weight: $font-400;
    line-height: 125%;
    letter-spacing: 0.5px;
  }
}
</style>
