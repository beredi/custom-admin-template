<template>
  <div :class="`${props.class}`">
    <div :class="`q-pa-md page-section ${props.childClass}`">
      <slot></slot>
    </div>
  </div>
</template>
<script setup>
const props = defineProps(["class", "childClass"]);
</script>
