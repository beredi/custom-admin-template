<template>
  <q-menu
    transition-show="jump-down"
    transition-hide="jump-up"
    class="header-menu-dropdown"
  >
    <q-list style="min-width: 100px">
      <q-item
        clickable
        v-close-popup
        @click="changeLanguage('en-US')"
        :class="activeLocale === 'en-US' ? 'bg-accent text-white' : null"
      >
        <q-item-section>English</q-item-section>
      </q-item>
      <q-item
        clickable
        v-close-popup
        @click="changeLanguage('sk')"
        :class="activeLocale === 'sk' ? 'bg-accent text-white' : null"
      >
        <q-item-section>Slovak</q-item-section>
      </q-item>
    </q-list>
  </q-menu>
</template>

<script setup>
import { computed } from "vue";
import { useI18n } from "vue-i18n";
const { locale, t } = useI18n({ useScope: "global" });

const changeLanguage = (lang) => {
  locale.value = lang;
};

const activeLocale = computed(() => locale.value);
</script>
