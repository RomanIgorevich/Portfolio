<template>
  <section class="skill">
    <div class="container">
      <div class="skill__inner">
        <h2 class="skill__title">Навыки и умения</h2>
        <div class="context-wrapper">
          <div class="context">
            <h3 class="skill__text">Профессиональные навыки:</h3>
            <ul
              class="ul-skill"
              v-for="skill in professionalSkills"
              :key="skill"
            >
              <li class="li-skill">{{ skill }}</li>
            </ul>
          </div>
          <div class="context">
            <h3 class="skill__text">Личные качества:</h3>
            <ul
              class="ul-skill"
              v-for="quality in personalQualities"
              :key="quality"
            >
              <li class="li-skill">{{ quality }}</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Skill",
  data() {
    return {
      professionalSkills: [
        "Знаю HTML5, CSS3;",
        "Пишу код на JavaScript;",
        "Использую фреймворки Vue.js, Nuxt.js;",
        "Верстаю по методологии BEM, адаптивно, кроссбраузерно;",
        "Применяю препроцессор SASS;",
        "Пишу валидный, аккуратный и чистый код, использую в работе линтеры ESLint, Prettier;",
        "Знаю, применяю Git;",
        "Работаю на Linux (Ubuntu), могу и на windows.",
      ],
      personalQualities: [
        "Аналитический склад ума;",
        "Ответственность;",
        "Внимание к деталям;",
        "Творческие способности;",
        "Пунктуальность;",
        "Умение работать в команде;",
        "Умение соизмерять уровень своих навыков и умений с возможностью решать поставленные задачи;",
        "Нацеленность на результат;",
        "Постоянное желание осваивать новые технологии и инструменты.",
      ],
    };
  },
};
</script>

<style lang="scss">
.skill {
  padding-top: $padding * 3;
}
.skill__inner {
  background: $fon;
  padding: $padding * 3;
  box-shadow: 0px 5px 15px 0px rgba(128, 127, 127, 0.3);
}
.skill__title {
  text-align: center;
  font-size: $font-size-title;
  padding-bottom: $padding/2;
}
.li-skill {
  list-style: inside;
  padding-left: 20px;
}
.skill__text {
  padding-top: $padding;
  padding-bottom: $padding/4;
}
</style>
