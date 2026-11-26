<template>
  <BApp>




    <header>

      <BNavbar variant="success" type="dark">
        <BNavbarBrand href="#navbar-brand-image-text">
          <img src="../public/logo/logo-mirabal.png" class="d-inline-block align-top" alt="Logo Mirabal" height="40" />
        </BNavbarBrand>
        <p>10 anos de luta</p>
      </BNavbar>

    </header>


    <router-view />
  </BApp>
</template>

<script setup>
import { BApp } from 'bootstrap-vue-next'
</script>
<style scoped lang="scss"></style>
