<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>
<template>
    <div class="container">
        <!-- <img src="../components/images/logo.jpg" class="logo" width="100px" alt=""> -->
        <h1>WELCOME</h1>
        <div class="btn">
          <RouterLink to='login' class="link">Get Started </RouterLink>
          <RouterLink to='scanqr' class="link qr">Scan QR </RouterLink>
        </div>
        <div class="image-bg">
          <div class="bg"></div>
          <!-- <img src="../components/images/dog.jpg" alt=""> -->
        </div>
    </div>
</template>