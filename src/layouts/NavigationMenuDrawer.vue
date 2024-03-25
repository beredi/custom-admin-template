<template>
  <q-drawer
    v-model="drawerModel"
    show-if-above
    :mini="!drawerModel || miniState"
    @click.capture="drawerClick"
    :width="300"
    :overlay="false"
    bordered
    class="navigation-drawer"
  >
    <q-scroll-area class="fit" :horizontal-thumb-style="{ opacity: 0 }">
      <q-list class="q-pa-lg">
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" />
          </q-item-section>

          <q-item-section class="text-h6">Quasar Framework</q-item-section>
        </q-item>

        <q-expansion-item
          expand-icon-class="text-accent"
          icon="email"
          label="Dashboards"
        >
          <q-card>
            <q-card-section>
              <q-item clickable v-ripple class="menu-item">
                <q-item-section avatar>
                  <q-icon name="inbox" />
                </q-item-section>

                <q-item-section> Inbox </q-item-section>
              </q-item>
            </q-card-section>
          </q-card>
        </q-expansion-item>
        <q-item clickable v-ripple class="menu-item">
          <q-item-section avatar>
            <q-icon name="inbox" />
          </q-item-section>

          <q-item-section> Inbox </q-item-section>
        </q-item>

        <q-item active clickable v-ripple class="menu-item">
          <q-item-section avatar>
            <q-icon name="star" />
          </q-item-section>

          <q-item-section> Star </q-item-section>
        </q-item>

        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon name="send" />
          </q-item-section>

          <q-item-section> Send </q-item-section>
        </q-item>

        <q-item clickable v-ripple class="menu-item">
          <q-item-section avatar>
            <q-icon name="drafts" />
          </q-item-section>

          <q-item-section> Drafts </q-item-section>
        </q-item>
      </q-list>
    </q-scroll-area>

    <!--
      in this case, we use a button (can be anything)
      so that user can switch back
      to mini-mode
    -->
    <div
      class="q-mini-drawer-hide absolute q-pa-sm menu-icon"
      style="top: 30px; right: -20px; border-radius: 50%"
    >
      <q-btn
        dense
        round
        unelevated
        color="accent"
        icon="chevron_left"
        size="sm"
        @click="miniState = true"
      />
    </div>
  </q-drawer>
</template>
<script setup>
import { ref, computed } from "vue";

const props = defineProps(["drawer"]);
const emits = defineEmits(["update:drawer"]);

const miniState = ref(false);

const drawerModel = computed({
  get() {
    return props.drawer;
  },
  set(value) {
    emits("update:drawer", value);
  },
});

const drawerClick = (e) => {
  // if in "mini" state and user
  // click on drawer, we switch it to "normal" mode
  if (miniState.value) {
    miniState.value = false;

    // notice we have registered an event with capture flag;
    // we need to stop further propagation as this click is
    // intended for switching drawer to "normal" mode only
    e.stopPropagation();
  }
};
</script>

<style lang="scss" scoped>
body.body--light {
  .navigation-drawer {
    background-color: white;
  }
  .menu-icon {
    background-color: $light-page;
  }
}
body.body--dark {
  .navigation-drawer {
    background-color: $dark;
  }
  .menu-icon {
    background-color: $dark-page;
  }
}

.menu-item {
  border-radius: 12px;
}
</style>
