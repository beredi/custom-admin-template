<template>
  <q-page padding class="flex flex-center">
    <h1>Test dark mode</h1>
    <q-btn @click="changeTheme">Change theme</q-btn>

    <h1>{{ $q.dark.isActive ? "YOu dark" : "You LIGHT" }}</h1>
  </q-page>
</template>

<script setup>
import { useQuasar } from "quasar";

const $q = useQuasar();

const changeTheme = () => {
  $q.dark.toggle();
};
</script>
