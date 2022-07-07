<template>
  <footer class="p-4 text-center">
    © {{ new Date().getFullYear() }} — Admin Tool by
    <a href="https://www.teamsolutions.am" target="_blank" class="footer-link">TeamSolutions.am</a>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style>
.footer-link{
  color: #48A3EA;
}

.footer-link:hover{
  color: #48A3EA;
}
</style>