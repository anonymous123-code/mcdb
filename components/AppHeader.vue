<template>
  <Link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"></Link>
  <div :class="`nav ${menuOpened ? 'expanded':''}`" id="myTopnav">
    <nuxt-link href="/" class="active">Home</nuxt-link>
    <nuxt-link href="/file-analyzer">File Analyzer</nuxt-link>
    <nuxt-link href="/mod-list-analyzer">Mod List Analyzer</nuxt-link>
    <nuxt-link href="/docs">Docs</nuxt-link>
    <nuxt-link href="/about">About</nuxt-link>
    <nuxt-link href="javascript:void(0);" class="icon" @click="menuOpened = !menuOpened">
      <i class="fa fa-bars"></i>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  name: "AppHeader",

  data() {
    return {
      menuOpened: false
    }
  }
}
</script>

<style scoped>
/* Add a black background color to the top navigation */
.nav {
  background-color: var(--nav-background);
  overflow: hidden;
  width: 100vw;
  top: 0;
  position: sticky;
  z-index: 5;
}

/* Style the links inside the navigation bar */
.nav a {
  float: left;
  display: block;
  color: var(--nav-link);
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

/* Change the color of links on hover */
.nav a:hover {
  background-color: var(--nav-link-hover-background);
  color: var(--nav-link-hover);
}

/* Add an active class to highlight the current page */
.nav a.router-link-exact-active {
  background-color: var(--nav-link-active-background);
  color: var(--nav-link-active);
}

/* Hide the link that should open and close the topnav on small screens */
.nav .icon {
  display: none;
}

/* When the screen is less than 600 pixels wide, hide all links, except for the first one ("Home"). Show the link that contains should open and close the topnav (.icon) */
@media screen and (max-width: 600px) {
  .nav a:not(.router-link-exact-active) {display: none;}
  .nav a.icon {
    display: block;
    position: absolute;
    right: 0;
    top: 0;
  }
  .nav a:not(.icon) {
    float: none;
    text-align: left;
  }
}

/* The "responsive" class is added to the topnav with JavaScript when the user clicks on the icon. This class makes the topnav look good on small screens (display the links vertically instead of horizontally) */
@media screen and (max-width: 600px) {
  .nav.expanded a {
    display: block;
  }
}
</style>