<template>
  <div>
    <navbar />
    <a name="info"></a>
    <info />
    <a name="skill"></a>
    <skill />
    <a name="portfolio"></a>
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
