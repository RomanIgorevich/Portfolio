<template>
  <section class="portfolio">
    <div class="container">
      <div class="portfolio__inners">
        <h2 class="portfolio__title">Портфолио</h2>
        <div class="portfolio__inner">
          <div
            class="portfolio__card-wrapper"
            v-for="work of myWorks"
            :key="work.img"
            @click="work.isModel = !work.isModel"
          >
            <div class="portfolio__card">
              <div class="img-wrapper">
                <img :src="require(`../assets/img/${work.img}`)" />
              </div>
              <h3>{{ work.title }}</h3>
              <p>{{ work.textSmall }}</p>
            </div>
          </div>
          <div v-for="work of myWorks" :key="work.img">
            <modal
              v-show="work.isModel"
              :dataWork="work"
              @close="work.isModel = false"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Modal from "./Modal.vue";
export default {
  name: "Portfolio",
  components: {
    Modal,
  },
  data() {
    return {
      myWorks: [
        {
          img: "1.png",
          title: "Консалтинг",
          textSmall: "Адаптивная верстка",
          textBig: "Адаптивная верстка одностраничного сайта по макету PSD.",
          stack: "HTML5, CSS3, JS, jQuery, BEM.",
          link: "https://romanigorevich.github.io/Adaptive-layout-1/",
          isModel: false,
        },
        {
          img: "7.png",
          title: "Waxa Shop",
          textSmall: "Адаптивная верстка",
          textBig: "Адаптивная верстка макета из Figma.",
          stack: "HTML5, CSS3, JS, BEM.",
          link: "https://romanigorevich.github.io/Adative-layout-2/",
          isModel: false,
        },
        {
          img: "2.png",
          title: "Заметки",
          textSmall: "Приложение с заметками",
          textBig:
            "В приложение с заметками реализованы: создание, редактирование и удаление заметок, можно выбирать приоритетность, делать поиск по заметкам.",
          stack: "HTML5, CSS3, SCSS, JS, VUE, VUE Cli.",
          link: "https://romanigorevich.github.io/Notes/",
          isModel: false,
        },
        {
          img: "3.png",
          title: "Модальные окна",
          textSmall: "Работа с модальными окнами",
          textBig:
            "При работе с модальными окнами реализованы: переиспользование компонентов, валидация полей, скрытие элементов при клике за область.",
          stack: "HTML5, SCSS, JS, VUE, Vuelidate.",
          link: "https://romanigorevich.github.io/Modals/",
          isModel: false,
        },
        {
          img: "4.png",
          title: "Блог",
          textSmall: "Разработка блога",
          textBig:
            "В этом проекте создан блог, написан полностью фронтенд, фронтенд для главный страницы и админ панели. Сделаны: посты; контактная форма; вывод единичного поста; комментарии которые могут выводить некоторые пользователи; страница блога, где выводятся все посты и страница обо мне; админ панель. В админ панели были реализованы: редактирование постов, добавление новых, модерирование комментариев. К комментариям можно добавлять статус, отображать их или нет, также комментарии можно удалять.",
          link: "https://romanigorevich.github.io/Blog/",
          stack: "HTML5, SCSS, JS, vue.js, Nuxt.js, axios, firebase.",
          isModel: false,
        },
        {
          img: "5.png",
          title: "Магазин монет",
          textSmall: "Интернет магазин по покупке монет",
          textBig:
            "В этом проекте создан интернет магазин, в котором реализованы: добавление, удаление и редактирование количества товаров в корзине; добавлена фильтрация по выбранному диапазону цен; подробное  описание товара; загрузка товаров определенных категорий.",
          stack: "HTML5, CSS3, JS, Vue.js, Axios, Vue-router, Vuex.",
          link: " https://romanigorevich.github.io/Coin-shop/",
          isModel: false,
        },
        {
          img: "6.png",
          title: "Конвертер валют",
          textSmall: "Тестовое задание",
          textBig:
            "Напиcал SPA для конвертирования валют. Приложение состоит из двух страниц: первая страница - конвертер из одной валюты в другую, вторая с текущими курсами валют.",
          stack: "SCSS, JS, Vue.js 3, Axios, Vue-router, Vuex.",
          link: "https://romanigorevich.github.io/my_projects/",
          isModel: false,
        },
        {
          img: "8.png",
          title: "Ювента-Крым",
          textSmall: "Адаптивная верстка",
          textBig: "Адаптивная верстка сайта по макету PSD.",
          stack: "HTML5, Sass, Jquery, Gulp, JS, BEM.",
          link: "https://romanigorevich.github.io/adaptive-layout-3/",
          isModel: false,
        },
      ],
    };
  },
};
</script>
