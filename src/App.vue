<template>
  <div>
    <navbar />
    <a name="info"></a>
    <info />
    <a class="indent" name="skill"></a>
    <skill />
    <a class="indent" name="portfolio"></a>
    <portfolio />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Info from "./components/Info.vue";
import Skill from "./components/Skill.vue";
import Portfolio from "./components/Portfolio.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Info,
    Skill,
    Portfolio,
  },
};
</script>

<style lang="scss">
.indent {
  display: block;
  content: "";
  height: 70px;
  margin: -70px 0 0 0;
}
</style>
