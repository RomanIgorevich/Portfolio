<template>
  <section class="navbar">
    <div class="container">
      <div class="navbar__inner">
        <ul id="menu__list" :class="{ 'active-menu': isActiveMenu }">
          <li class="menu__item" v-for="link in menuList" :key="link">
            <a
              class="menu__link"
              :href="link.href"
              @click="isActiveMenu = !isActiveMenu"
              >{{ link.name }}</a
            >
          </li>
        </ul>
        <div class="menu__link-btn" @click="isActiveMenu = !isActiveMenu"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      isActiveMenu: false,
      menuList: [
        { href: "#info", name: "Главная" },
        { href: "#skill", name: "Навыки и умения" },
        { href: "#portfolio", name: "Портфолио" },
      ],
    };
  },
};
</script>
