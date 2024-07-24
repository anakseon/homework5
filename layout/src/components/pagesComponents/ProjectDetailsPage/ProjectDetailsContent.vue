<template>
  <div class="project-details__content center">
    <h2 class="project-details__header">Минималистичные спальни</h2>
    <p class="project-details__text">В своей статье от 1994-го года журнал «Before & After» отследил фразу «Lorem ipsum ...» до философского трактата Цицерона О пределах добра и зла, написанного в 45 году до нашей эры на латинском языке. 
      <br><br>
      В оригинале текст выглядит так «Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit ...», и переводится как «Нет никого, кто любил бы свою боль, кто искал бы ее и хотел бы чтобы она была у него. Потому что это боль...». 
    </p>
    <ProjectDetailsSlider />
  </div>
</template>

<script>
import ProjectDetailsSlider from './ProjectDetailsSlider.vue'
export default {
  components: { ProjectDetailsSlider },
  name: 'ProjectDetailsContent'
}
</script>

<style lang="scss" scoped>
@import "../../../scss/vars";

.project-details {
  &__content {
    margin-top: 200px;
    margin-bottom: 200px;
  }

  &__header {
    text-align: center;
    color: #292F36;
    font-family: $familyTitle;
    font-size: 50px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    letter-spacing: 1px;
  }

  &__text {
    margin-top: 11px;
    padding-left: calc(($widthSite - 670px) / 2);
    padding-right: calc(($widthSite - 670px) / 2);
    text-align: justify;
    margin-bottom: 100px;
    color: #4D5053;
    font-family: $familyText;
    font-size: 22px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 150%;
    letter-spacing: 0.22px;
  }
}
</style>
