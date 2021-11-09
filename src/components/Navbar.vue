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

<style lang="scss">
.navbar {
  background: $background-navbar;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 4;
}
.navbar::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: $background-navbar;
  z-index: 2;
}
.navbar__inner {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  height: $height-navbar;
  padding: 0;
}
#menu__list {
  display: flex;
  justify-content: flex-end;
  z-index: 2;
}
.menu__item + .menu__item {
  padding-left: $padding;
}
.menu__link {
  display: block;
  line-height: 42px !important;
  text-transform: uppercase;
  color: $background;
  transition: all 0.5s;
  border-bottom: 1px solid transparent;
  z-index: 2;
}
.menu__link:hover {
  color: $color-hover;
}
.menu__link-btn {
  display: none;
  z-index: 5;
  cursor: pointer;
  position: relative;
}
.menu__link-btn::before {
  content: url("../assets/svg/menu.svg");
  position: absolute;
  top: -12px;
  right: 0;
}
#menu__list.active-menu {
  top: 50px;
}
</style>
