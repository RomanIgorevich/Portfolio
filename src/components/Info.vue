<template>
  <section class="info">
    <div class="container">
      <div class="info__inner">
        <div class="info__inner-left">
          <img src="../assets/img/I.jpg" />
        </div>
        <div class="info__inner-right">
          <h2 class="info__title">Фесенко Роман</h2>
          <p class="info__text">Фронтенд разработчик</p>
          <div class="contacts">
            <a v-for="link in contactsList" :key="link" :class="link.class" :href="link.href">{{ link.name }}</a>
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

<style lang="scss">
.info {
  padding-top: 142px;
  background-image: url(../assets/img/fon.jpg);
  background-repeat: no-repeat;
  background-size: 100%;
}
.info__inner {
  background: $fon;
  padding: $padding * 3;
  display: flex;
  justify-content: space-between;
  box-shadow: 0px 5px 15px 0px rgba(128, 127, 127, 0.3);
}
.info__inner-left {
  width: 50%;
  align-items: center;
  display: flex;
  box-shadow: 0px 5px 15px 0px rgba(128, 127, 127, 0.2);
}
.info__inner-left img {
  width: 100%;
  margin: auto;
}
.info__inner-right {
  padding-left: $padding * 3;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 50%;
}
.info__title {
  text-align: center;
  font-size: $font-size-title;
  padding-bottom: $padding/2;
}
.info__text {
  text-align: center;
  padding-bottom: $padding;
  font-size: $font-size-text;
}
.phone,
.mail,
.telegram,
.github {
  display: block;
  position: relative;
  padding-left: 30px;
  color: $color;
}
.phone::before {
  content: url("../assets/svg/phone.svg");
  position: absolute;
  top: 3px;
  left: 0;
}
.mail::before {
  content: url("../assets/svg/envelop.svg");
  position: absolute;
  top: 3px;
  left: 0;
}
.github::before {
  content: url("../assets/svg/github.svg");
  position: absolute;
  top: 4px;
  left: 0;
}
.telegram::before {
  content: url("../assets/svg/telegram.svg");
  position: absolute;
  top: 4px;
  left: 0;
}
</style>
