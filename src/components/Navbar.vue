<script setup lang="ts">
import { ref } from 'vue'
let mobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value;
};
</script>


<template>
  <div class="nav-wrapper">
    <div class="mobileNav">
      <img src="/logo.png">
      <div class="mobile-menu-icon" @click="toggleMobileMenu">
        <div class="bar"></div>
        <div class="bar"></div>
        <div class="bar"></div>
      </div>
      <nav v-if="mobileMenuOpen" class="mobile-nav-list">
        <ul class="mobilelinks" :class="{ 'show-mobile-menu': mobileMenuOpen }">
          <li>About Us</li>
          <li>Pricing</li>
          <li>Product</li>
          <li>Support</li>
          <li>
            <div class="button">Get PressOne</div>

          </li>
        </ul>
        <svg @click="mobileMenuOpen = !mobileMenuOpen" xmlns="http://www.w3.org/2000/svg" width="32" height="32"
          viewBox="0 0 24 24">
          <path fill="currentColor"
            d="M19 6.41L17.59 5L12 10.59L6.41 5L5 6.41L10.59 12L5 17.59L6.41 19L12 13.41L17.59 19L19 17.59L13.41 12L19 6.41z" />
        </svg>
      </nav>
    </div>
    <div class="desktop-nav">
      <nav class="nav">
        <img src="/logo.png">
        <ul class="desktopLinks">
          <li>About Us</li>
          <li>Pricing</li>
          <li>Product</li>
          <li>Support</li>
        </ul>
        <div class="desktop-button">
          <span>Get PressOne</span>
        </div>
      </nav>
    </div>
  </div>
</template>

<style scoped>
.nav-wrapper {
  padding-inline: 19px;

}

.mobile-nav-list {
  display: none;
}


.mobileNav {
  display: none;
}

.links {
  list-style-type: none;
  display: flex;
  gap: 13px;
}

.desktopLinks {
  display: flex;
  gap: 12px;
  font-size: 16px;
}

.desktop-button {
  height: 30px;
  text-align: center;
  border: 1px solid #0E99D2;
  display: flex;
  align-items: center;
  color: #0E99D2;
  padding-inline: 20.5px;
  border-radius: 4px;
  margin-right: 40px;
  background-color: white;
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

/* Mobile menu styles */

.desktop-nav {
  display: flex;
  align-items: center;
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  z-index: 100;
  background-color: white;
  padding-inline: 20px;
  padding-top: 10px;
}

.desktop-nav>.nav {
  display: flex;
  justify-content: space-between;
  width: 100%;
  height: 60px;
}

.desktop-nav>.nav>img {
  height: 38px;
  width: 48px;
}

.bar {
  width: 25px;
  height: 3px;
  background-color: #0E99D2;
  margin: 4px 0;
  border-radius: 2px;
}



ul {
  list-style-type: none;
}


@media (max-width: 768px) {
  .mobile-menu-icon {
    display: flex;
    cursor: pointer;
    flex-direction: column;
    margin-right: 15px;
    margin-top: 12px;
  }

  .desktop-nav {
    display: none;
  }

  svg {
    margin-right: 20px;
    margin-top: 10px;
    display: block;
    color: white;
  }

  ul {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .mobile-nav-list {
    display: flex;
    position: absolute;
    right: 0;
    background-color: #0E99D2;
    width: 100%;
    top: 0;
    justify-content: space-between;
  }

  .mobileNav {
    display: flex;
    justify-content: space-between;
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    z-index: 100;
  }

  .mobileNav>img {
    margin-left: 20px;
    margin-top: 12px;
  }

  .nav-wrapper {
    padding-inline: 0px;

  }
}
</style>


