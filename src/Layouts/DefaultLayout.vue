<script setup lang="ts"></script>

<template>
  <div>default layout is alive</div>

  <div id="navigation-app-bar-top"></div>

  <div id="navigation-sidebar-left"></div>

  <div id="navigation-sidebar-right"></div>

  <div id="main-page-view">
    <router-view />
  </div>

  <div id="navigation-app-bar-bottom"></div>
</template>
