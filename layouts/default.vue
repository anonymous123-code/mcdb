<template>
<div class="wrapper">
  <AppHeader/>
  <div style="min-height: calc(100vh - 100px)"><slot/></div>
  <AppFooter/>
</div>
</template>

<script>
import AppFooter from "~/components/AppFooter.vue";
import AppHeader from "~/components/AppHeader.vue";

export default {
  name: "default",
  components: {AppHeader, AppFooter}
}
</script>

<style>
body {
  margin: 0;
  font-family: ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,Noto Sans,sans-serif,"Apple Color Emoji","Segoe UI Emoji",Segoe UI Symbol,"Noto Color Emoji";
  line-height: 1.5;
  background-color: var(--background);
}

div.wrapper {
  min-height: 100vh;
}
</style>