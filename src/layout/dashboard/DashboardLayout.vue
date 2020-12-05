<template>
  <div class="wrapper">
    <side-bar>
      <template slot="links">
        <sidebar-link to="/dashboard" name="Inicio" icon="tim-icons icon-chart-pie-36"/>
        <sidebar-link to="/articles" name="Usuarios" icon="tim-icons icon-atom"/>
        <sidebar-link to="/categories" name="Categorias" icon="tim-icons icon-pin"/>
        <sidebar-link to="/users" name="Usuarios" icon="tim-icons icon-bell-55"/>
        <sidebar-link to="/pos" name="Punto de Venta" icon="tim-icons icon-single-02"/>
      </template>
    </side-bar>
    <div class="main-panel">
      <top-navbar></top-navbar>

      <dashboard-content @click.native="toggleSidebar">

      </dashboard-content>

      <content-footer></content-footer>
    </div>
  </div>
</template>
<style lang="scss">
</style>
<script>
import TopNavbar from "../shared/TopNavbar.vue";
import ContentFooter from "./ContentFooter.vue";
import DashboardContent from "./Content.vue";
import MobileMenu from "./MobileMenu";
export default {
  components: {
    TopNavbar,
    ContentFooter,
    DashboardContent,
    MobileMenu
  },
  methods: {
    toggleSidebar() {
      if (this.$sidebar.showSidebar) {
        this.$sidebar.displaySidebar(false);
      }
    }
  }
};
</script>
