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
      <q-btn v-if="isDark" flat round class="button-header" @click="toggleTheme">
        <q-icon name="nights_stay" />
      </q-btn>
      <q-btn v-else flat round class="button-header" @click="toggleTheme">
        <q-icon name="light_mode" />
      </q-btn>
      <q-btn-dropdown icon="translate" text-color="accent" rounded flat>
        <q-list>
          <q-item clickable v-close-popup>
            <q-item-section>
              <q-item-label>English</q-item-label>
            </q-item-section>
          </q-item>

          <q-item clickable v-close-popup>
            <q-item-section>
              <q-item-label>Slovak</q-item-label>
            </q-item-section>
          </q-item>
        </q-list>
      </q-btn-dropdown>
      <q-btn flat round class="button-header"><q-icon name="grid_view" /></q-btn>
      <q-btn flat round class="button-header">
        <q-icon name="notifications" />
        <q-badge
          color="negative"
          text-color="white"
          label="2"
          class="notification-badge"
        />
      </q-btn>
      <q-btn flat round class="button-header"><q-icon name="person " /></q-btn>
    </q-toolbar>
  </q-header>
</template>
<script setup>
import { useQuasar } from "quasar";
import { computed } from "vue";
import { ref } from "vue";
const props = defineProps(["drawer"]);
const emits = defineEmits(["toggleLeftDrawer"]);

const $q = useQuasar();

const isDark = computed(() => $q.dark.isActive);

const toggleTheme = () => {
  $q.dark.toggle();
};

const search = ref("");
</script>
