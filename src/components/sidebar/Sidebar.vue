<script>
import SidebarLink from "../sidebar/SidebarLink";
import { collapsed, toggleSidebar, sidebarWidth } from "./state";
export default {
  props: {},
  components: { SidebarLink },
  setup() {
    return { collapsed, toggleSidebar, sidebarWidth };
  },
};
</script>

<template>
  <div class="sidebar" :style="{ width: sidebarWidth }">
    <h1>
      <span v-if="collapsed">
        <div>V</div>
        <div>S</div>
      </span>
      <span v-else>Restauranti</span>
    </h1>

    <!-- <SidebarLink to="/" icon="fas fa-home">Home</SidebarLink> -->
    <SidebarLink to="/admin/menu" icon="fas fa-chart-bar">Insert your menu</SidebarLink>
    <SidebarLink to="/admin/analyze" icon="fas fa-users">Analytique</SidebarLink>
    <SidebarLink to="/admin/order" icon="fas fa-image">Orders</SidebarLink>
    <!-- <SidebarLink to="/admin/cart" icon="fas fa-image">cart</SidebarLink> -->
    <SidebarLink to="/admin" icon="fas fa-image">Log out</SidebarLink>



    <span
      class="collapse-icon"
      :class="{ 'rotate-180': collapsed }"
      @click="toggleSidebar"
    >
      <i class="fas fa-angle-double-left" />
    </span>
  </div>
</template>

<style scoped>
.bottom {
  position: absolute;
  bottom: 10px;
}
.sidebar {
  color: white;
  background-color: #f0e5d5;
  float: left;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  bottom: 0;
  padding: 0.5em;
  transition: 0.3s ease;
  display: flex;
  flex-direction: column;
}
.sidebar h1 {
  height: 2.5em;
  font-weight: bold;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  color: black;
}
.collapse-icon {
  position: absolute;
  bottom: 0;
  padding: 0.75em;
  color: rgba(255, 255, 255, 0.7);
  transition: 0.2s linear;
}
.rotate-180 {
  transform: rotate(180deg);
  transition: 0.2s linear;
}
</style>
