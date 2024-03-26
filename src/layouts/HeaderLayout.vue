<template>
  <q-header class="q-mx-md q-my-md">
    <q-toolbar class="toolbar q-py-xs q-px-sm">
      <q-btn
        dense
        flat
        round
        icon="menu"
        @click="emits('toggleLeftDrawer', !props.drawer)"
      />

      <q-input borderless v-model="search" label="Search" class="q-ml-lg">
        <template v-slot:prepend> <q-icon name="search" /> </template>
      </q-input>
      <q-space />
      <q-btn
        v-if="isDark"
        flat
        round
        class="button-header"
        @click="toggleTheme"
      >
        <q-icon name="nights_stay" />
      </q-btn>
      <q-btn v-else flat round class="button-header" @click="toggleTheme">
        <q-icon name="light_mode" />
      </q-btn>
      <q-btn icon="translate" text-color="accent" flat>
        <language-menu></language-menu>
      </q-btn>
      <q-btn flat round class="button-header">
        <q-icon name="grid_view" />
      </q-btn>
      <q-btn icon="notifications" class="button-header" flat round>
        <q-badge
          color="negative"
          text-color="white"
          label="2"
          class="notification-badge"
        />
        <notifications-menu></notifications-menu>
      </q-btn>
      <q-btn flat round class="button-header">
        <q-img
          src="../assets/female.jpg"
          spinner-color="white"
          style="height: 35px; max-width: 35px"
          class="profile-image"
        />
        <q-badge color="positive" class="notification-badge" rounded />
        <profile-menu></profile-menu>
      </q-btn>
    </q-toolbar>
  </q-header>
</template>
<script setup>
import { useQuasar } from "quasar";
import { computed } from "vue";
import { ref } from "vue";
import NotificationsMenu from "./components/NotificationsMenu.vue";
import LanguageMenu from "./components/LanguageMenu.vue";
import ProfileMenu from "./components/ProfileMenu.vue";
const props = defineProps(["drawer"]);
const emits = defineEmits(["toggleLeftDrawer"]);

const $q = useQuasar();

const isDark = computed(() => $q.dark.isActive);

const toggleTheme = () => {
  $q.dark.toggle();
};

const search = ref("");
</script>
