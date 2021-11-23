<template>
  <div id="app">
    <v-header />
    <top-nav />
    <main>
      <left-menu />
      <transition name="fade">
        <router-view msg="Welcome to Your Vue.js App" />
      </transition>
    </main>
    <v-footer />
  </div>
</template>

<script>
import VHeader from "@/layout/VHeader";
import TopNav from './components/TopNav.vue';
import LeftMenu from './components/LeftMenu.vue';
import VFooter from '@/layout/VFooter.vue';

export default {
  name: "App",
  components: {
    VHeader,
    TopNav,
    LeftMenu,
    VFooter,
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;900&display=swap');

* {
  margin: 0;
  padding: 0;
  font-family: "Montserrat";
  font-size: 14px;
  line-height: 130%;
  box-sizing: border-box;
}
:root {
  --main-color: #15499F;
  --main-color-light: #0584AC;
  --black: #040B1E;
  --second-color: #1BBDD4;
  --gray: #EAEAEA;
  --gray-background: #F5F5F5;
}
a {
  text-decoration: none;
  color: inherit;
}
button {
  border: 0;
}
button:hover {
  cursor: pointer;
}
.flex {
  display: flex;
}
li {
  list-style-type: none;
}
.section-title {
  font-size: 24px;
  font-weight: 500;
}
#app {
  max-width: 1600px;
  margin: 0 auto;
  color: var(--black);
}
main {
  display: inline-flex;
  flex-wrap: wrap;
  margin: 40px -20px 0 -20px;
  width: calc(100% + 20px);
}
main > * {
  margin: 0 20px 0 20px;
}
.fade-enter-active, .fade-leave-active {
  transition-property: opacity;
  transition-duration: .25s;
}
.fade-enter-active {
  transition-delay: .25s;
}
.fade-enter, .fade-leave-active {
  opacity: 0;
}
</style>
