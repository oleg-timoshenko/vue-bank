<template>
  <the-navbar></the-navbar>
  <the-sidebar></the-sidebar>
  <div class="container with-nav">
    <app-message />
    <router-view></router-view>
  </div>
</template>

<script>
import TheNavbar from "../components/TheNavbar";
import TheSidebar from "../components/TheSidebar";
import AppMessage from "../components/ui/AppMessage";


export default {
  components: {TheNavbar,TheSidebar , AppMessage}
}
</script>

<style scoped>

</style>