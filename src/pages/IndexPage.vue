<template>
  <page-layout>
    <page-section class="col-12">
      <h1 class="text-h5 q-px-none q-py-xs">Custom admin template</h1>
    </page-section>
    <page-section class="col-4">
      <q-icon name="sentiment_satisfied_alt" color="warning" size="lg" />
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam non
        auctor diam. Duis efficitur, ante id sagittis blandit, leo dolor varius
        arcu, nec cursus odio leo ac massa. Etiam pretium metus ac mattis
        cursus. Nullam nibh leo, mollis in nibh eu, egestas auctor lacus. Donec
        ultricies pulvinar urna. Cras id interdum augue.
      </p>
    </page-section>
    <page-section class="col-8" childClass="bg-accent text-white">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam non
        auctor diam. Duis efficitur, ante id sagittis blandit, leo dolor varius
        arcu, nec cursus odio leo ac massa. Etiam pretium metus ac mattis
        cursus. Nullam nibh leo, mollis in nibh eu, egestas auctor lacus. Donec
        ultricies pulvinar urna. Cras id interdum augue.
      </p>
    </page-section>
  </page-layout>
</template>

<script setup>
import { useQuasar } from "quasar";
import PageSection from "../layouts/components/PageSection.vue";
import PageLayout from "../layouts/PageLayout.vue";

const $q = useQuasar();

const changeTheme = () => {
  $q.dark.toggle();
};
</script>
