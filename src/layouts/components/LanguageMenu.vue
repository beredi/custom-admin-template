<template>
  <q-menu
    transition-show="jump-down"
    transition-hide="jump-up"
    class="header-menu-dropdown"
  >
    <q-list style="min-width: 100px">
      <q-item clickable v-close-popup>
        <q-item-section>English</q-item-section>
      </q-item>
      <q-item clickable v-close-popup>
        <q-item-section>Slovak</q-item-section>
      </q-item>
    </q-list>
  </q-menu>
</template>

<script setup></script>
