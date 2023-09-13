<script setup lang="ts">

</script>

<template>
  <div class="nav-wrapper">
    <nav class="nav">
      <img src="/logo.png">
      <ul class="links">
        <li>About Us</li>
        <li>Pricing</li>
        <li>Product</li>
        <li>Support</li>
      </ul>
      <div class="button">Get PressOne</div>
    </nav>
  </div>
</template>

<style scoped>
.nav-wrapper {
  padding-inline: 80px;

}

.nav {
  display: flex;
  margin-top: 22px;
  width: 100%;
  justify-content: space-between;
}

.links {
  list-style-type: none;
  display: flex;
  gap: 13px;
}

.button {
  border: 1px solid #0E99D2;
  background-color: white;
  color: #0E99D2;
  cursor: pointer;
  padding-inline: 20.5px;
  padding-block: 14px !important;
  border-radius: 4px;
}
</style>
