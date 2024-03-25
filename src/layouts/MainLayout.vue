<template>
  <q-layout view="lHh lpR fFf">
    <header-layout
      :drawer="drawer"
      @toggleLeftDrawer="updateDrawer"
    ></header-layout>
    <navigation-menu-drawer
      :drawer="drawer"
      @update:drawer="updateDrawer"
    ></navigation-menu-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from "vue";
import HeaderLayout from "./HeaderLayout.vue";
import NavigationMenuDrawer from "./NavigationmenuDrawer.vue";

const drawer = ref(false);

const updateDrawer = (value) => {
  drawer.value = value;
};
</script>
