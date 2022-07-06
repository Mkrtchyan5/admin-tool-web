<template>
  <b-navbar-brand href="/admin/starter">
    <div class="logo">
      <!-- Logo icon -->
      <b class="logo-icon">
        <img src="../../../assets/images/tool.png" alt="homepage">
      </b>

      <span class="logo-text mt15">
            <!-- Light Logo text -->
            <h2 style="color: black">Admin Tool</h2>
      </span>
    </div>
  </b-navbar-brand>
</template>

<script>
export default {
  name: 'LogoDark',
}
</script>
<style scoped>
.logo {
  margin-top: 10px;
  display: flex;
}

.mt15 {
  margin-top: 15px;
}
</style>