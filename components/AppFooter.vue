<template>
<div>
  <hr>
  <NuxtLink to="https://anonymous123-code.github.io/">by anonymous123-code</NuxtLink>
  <NuxtLink to="">view the source code on GitHub</NuxtLink>
  <NuxtLink to="">hosted using Cloudflare Pages</NuxtLink>
</div>
</template>

<script>
export default {
  name: "AppFooter"
}
</script>

<style scoped>
a {
  display: block;
  color: var(--footer-color);
}

div {
  display: flex;
  align-items: center;
  flex-direction: column;
  padding: 0 30px 30px 30px;
}

hr {
  width: 95vw;
  max-width: 500px;
}
</style>