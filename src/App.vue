<template>
  <div>
    <section class="grid grid-template-areas-1" :class="{ 'grid-open-menu': isExpanded }">
      <div class="nav">
        <Navbar :isExpanded="isExpanded" @open-menu="openMenu"/>
      </div>
      <div class="content">
        <router-view/>
      </div>
      <div class="sidenav">
        <Sidebar :isExpanded="isExpanded" @close-menu="closeMenu"/>
      </div>
      <div class="footer">
          teste
      </div>
    </section>
  </div>
</template>

<script>
import Sidebar from "./components/Sidebar.vue";
import Navbar from "./components/Navbar.vue";

export default {
  data() {
    return {
      isExpanded: false
    }
  },
  components: {
    Sidebar,
    Navbar,
  },
  methods: {
    openMenu(open) {
      this.isExpanded = open;
    },
  },
}
</script>

<style>
body {
  margin: 0;
}

.grid {
	display: grid;
  grid-template-columns: 60px 1fr 1fr;
  grid-template-rows: repeat(4, auto);
  transition: all .5s ease-in-out;
}

.grid-open-menu {
  grid-template-columns: 250px 1fr 1fr;
}

.nav {
	grid-area: nav;
}

.content {
  background: red;
	grid-area: content;
  height: 70%;
}

.sidenav {
  background: green;
	grid-area: sidenav;
  max-width: 240px; 
}

.footer {
  background: aquamarine;
	grid-area: footer;
}

.grid-template-areas-1 {
	grid-template-areas:
		"sidenav nav nav"
		"sidenav content content"
		"sidenav content content"
		"sidenav footer footer"
		;
}

</style>
