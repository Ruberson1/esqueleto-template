<template>
  <div class="home">
    <nav class="main-menu" :class="{ expanded: isExpanded }">
      <ul class="mt-47 ps-0">
        <li>
          <router-link :to="{path: '/'}">
            <i class="fa fa-home fa-2x"></i>
            <span class="nav-text">Dashboard </span>
          </router-link>
        </li>
        <li class="has-subnav">
          <router-link :to="{name: 'Teste'}">
            <i class="fa fa-globe fa-2x"></i>
            <span class="nav-text"> Community Dashboard </span>
          </router-link>
        </li>
        <li class="has-subnav">
          <a href="#">
            <i class="fa fa-comments fa-2x"></i>
            <span class="nav-text"> Group Hub Forums </span>
          </a>
        </li>
        <li class="has-subnav">
          <a href="#">
            <i class="fa fa-camera-retro fa-2x"></i>
            <span class="nav-text"> Survey Photos </span>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="fa fa-film fa-2x"></i>
            <span class="nav-text"> Surveying Tutorials </span>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="fa fa-book fa-2x"></i>
            <span class="nav-text"> Surveying Jobs </span>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="fa fa-cogs fa-2x"></i>
            <span class="nav-text"> Tools & Resources </span>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="fa fa-map-marker fa-2x"></i>
            <span class="nav-text"> Member Map </span>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="fa fa-info fa-2x"></i>
            <span class="nav-text"> Documentation </span>
          </a>
        </li>
      </ul>

      <ul class="logout ps-0" :class="isExpanded ? 'mt-0' : 'mt-47'">
        <li>
          <a href="#">
            <i class="fa fa-power-off fa-2x"></i>
            <span class="nav-text"> Logout </span>
          </a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  props: {
    isExpanded: {
      Type: Boolean
    }
  },
  methods: {
  },
};
</script>

<style scoped>
.fa {
  position: relative;
  display: table-cell;
  width: 60px;
  height: 36px;
  text-align: center;
  vertical-align: middle;
  font-size: 20px;
}

.expanded {
  width: 250px !important;
  overflow: visible;
}

.main-menu {
  background: #212529;
  border-right: 1px solid #e5e5e5;
  position: absolute;
  top: 0;
  bottom: 0;
  height: 100%;
  left: 0;
  width: 60px;
  overflow: hidden;
  -webkit-transition: width 0.05s linear;
  transition: width 0.05s linear;
  -webkit-transform: translateZ(0) scale(1, 1);
  z-index: 1000;
  transition: all .5s ease-in-out;
}

.main-menu li {
  position: relative;
  display: block;
  width: 250px;
}

.main-menu li > a {
  position: relative;
  display: table;
  border-collapse: collapse;
  border-spacing: 0;
  color: #999;
  font-family: arial;
  font-size: 14px;
  text-decoration: none;
  -webkit-transform: translateZ(0) scale(1, 1);
  -webkit-transition: all 0.1s linear;
  transition: all 0.1s linear;
}

.main-menu .nav-icon {
  position: relative;
  display: table-cell;
  width: 60px;
  height: 36px;
  text-align: center;
  vertical-align: middle;
  font-size: 18px;
}

.main-menu .nav-text {
  position: relative;
  display: table-cell;
  vertical-align: middle;
  width: 190px;
  font-family: "Titillium Web", sans-serif;
}

.main-menu > ul.logout {
  position: absolute;
  left: 0;
  bottom: 0;
}

.no-touch .scrollable.hover {
  overflow-y: hidden;
}

.no-touch .scrollable.hover:hover {
  overflow-y: auto;
  overflow: visible;
}

a:hover,
a:focus {
  text-decoration: none;
}

nav {
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  -o-user-select: none;
  user-select: none;
}

.main-menu li:hover > a,
nav.main-menu li.active > a,
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus,
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus,
.no-touch .dashboard-page nav.dashboard-menu ul li:hover a,
.dashboard-page nav.dashboard-menu ul li.active a {
  color: #fff;
  background-color: #000000;
}
.area {
  float: left;
  background: #e2e2e2;
  width: 100%;
  height: 100%;
}
@font-face {
  font-family: "Titillium Web";
  font-style: normal;
  font-weight: 300;
  src: local("Titillium WebLight"), local("TitilliumWeb-Light"),
    url(http://themes.googleusercontent.com/static/fonts/titilliumweb/v2/anMUvcNT0H1YN4FII8wpr24bNCNEoFTpS2BTjF6FB5E.woff)
      format("woff");
}
</style>
