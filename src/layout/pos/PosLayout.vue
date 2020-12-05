<template>
  <div class="wrapper">
      <div class="main-panel">
        <top-navbar></top-navbar>
        <div class="content-pos">
            <router-view></router-view>
        </div>
      </div>
  </div>
</template>

<script>

import TopNavbar from "../shared/TopNavbar.vue";

export default {
    components: {
        TopNavbar
    }
}
</script>

<style>

</style>