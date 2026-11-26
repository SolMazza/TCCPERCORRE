<template>

  <header>
    <BNavbar toggleable="lg" type="light" variant="light" class="shadow-sm">

      <!-- 1. LOGO E TEXTO (Esquerda) -->
      <BNavbarBrand href="/" class="d-flex align-items-center">
        <!-- Coloque o caminho da sua imagem aqui -->
        <img src="../public/logo/logo-mirabal.png" alt="Logo Mirabal - foto das 3 irmãs mirabais" height="40" class="me-2" />
        <span class="fw-bold">10 anos de luta</span>
      </BNavbarBrand>

      <!-- Botão para mobile (hambúrguer) -->
      <BNavbarToggle target="nav-collapse" />

      <!-- 2. AS ABAS (Direita / Centro) -->
      <BCollapse id="nav-collapse" is-nav>
        <!-- O 'ms-auto' empurra as abas para a direita. 
           Se quiser no centro, remova o 'ms-auto' e use 'mx-auto' -->
        <BNav tabs class="ms-auto" fill>



          <BNavItem>
            <RouterLink to="/" custom v-slot="{ navigate, href, isActive }">
              <a :href="href" @click="navigate" class="nav-link" :class="{ active: isActive }">
                Home
              </a>
            </RouterLink>
          </BNavItem>

          <BNavItem>
            <RouterLink to="/historia" custom v-slot="{ navigate, href, isActive }">
              <a :href="href" @click="navigate" class="nav-link" :class="{ active: isActive }">
                História
              </a>
            </RouterLink>
          </BNavItem>

          <BNavItem>
            <RouterLink to="/apoie" custom v-slot="{ navigate, href, isActive }">
              <a :href="href" @click="navigate" class="nav-link" :class="{ active: isActive }">
                Apoie
              </a>
            </RouterLink>
          </BNavItem>
          <BNavItem>
            <RouterLink to="/acoes" custom v-slot="{ navigate, href, isActive }">
              <a :href="href" @click="navigate" class="nav-link" :class="{ active: isActive }">
                Ações
              </a>
            </RouterLink>
          </BNavItem>

          <BNavItem>
            <RouterLink to="/festival-mirabal" custom v-slot="{ navigate, href, isActive }">
              <a :href="href" @click="navigate" class="nav-link" :class="{ active: isActive }">
                Festival <br/> Mirabal
              </a>
            </RouterLink>
          </BNavItem>

          <BNavItem>
            <RouterLink to="/contato" custom v-slot="{ navigate, href, isActive }">
              <a :href="href" @click="navigate" class="nav-link" :class="{ active: isActive }">
                Contato
              </a>
            </RouterLink>
          </BNavItem>

        </BNav>
      </BCollapse>

    </BNavbar>
  </header>


  <BApp>
    <router-view />
  </BApp>
</template>

<style scoped lang="scss"></style>
<script setup>
import { BApp } from 'bootstrap-vue-next'
</script>
