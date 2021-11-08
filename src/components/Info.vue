<template>
  <section class="info">
    <div class="container">
      <div class="info__inner">
        <div class="info__inner-left">
          <img src="../assets/img/I.jpg" />
        </div>
        <div class="info_inner-right">
          <h2 class="info__title">Фесенко Роман</h2>
          <p class="info__text">Фронтенд разработчик</p>
          <div class="contacts" v-for="link in contactsList" :key="link">
            <a :class="link.class" :href="link.href">{{ link.name }}</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Info",
  data() {
    return {
      contactsList: [
        {
          href: "tel:+79780415342",
          name: "+7 (978) 041 53 42",
          class: "phone",
        },
        {
          href: "mailto:roman.igorevich.ru@gmail.com",
          name: "roman.igorevich.ru@gmail.com",
          class: "mail",
        },
        {
          href: "https://github.com/RomanIgorevich",
          name: "github.com/RomanIgorevich",
          class: "github",
        },
        {
          href: "https://tlgg.ru/@FesenkoRoman",
          name: "@FesenkoRoman",
          class: "telegram",
        },
      ],
    };
  },
};
</script>
