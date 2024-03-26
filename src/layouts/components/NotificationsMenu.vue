<template>
  <q-menu
    transition-show="jump-down"
    transition-hide="jump-up"
    class="header-menu-dropdown"
  >
    <div style="min-width: 360px">
      <div class="row no-wrap q-pa-md justify-between items-center">
        <span class="text-h6">Notifications</span>
        <q-btn icon="mark_email_read" flat>
          <q-tooltip> Mark all as read </q-tooltip></q-btn
        >
      </div>
      <q-separator />
      <div class="q-py-md q-px-sm row no-wrap items-center notification-row">
        <q-img
          src="../../assets/male.jpg"
          spinner-color="white"
          style="height: 45px; max-width: 45px"
          class="profile-image"
        />
        <div class="column q-px-lg full-width">
          <span class="text-subtitle2 text-weight-bold">
            Congratulation Flora! 🎉
          </span>
          <span class="text-weight-light text-caption"
            >Won the monthly best seller badge</span
          >
          <span class="text-weight-thin">Today</span>
        </div>
        <div class="column justify-between items-center">
          <q-btn
            icon="close"
            flat
            size="sm"
            class="notification-close-button q-px-sm"
          />
          <div class="q-my-sm q-px-sm">
            <q-badge color="accent" rounded />
          </div>
        </div>
      </div>
      <div class="q-py-md q-px-sm row no-wrap items-center notification-row">
        <q-img
          src="../../assets/female.jpg"
          spinner-color="white"
          style="height: 45px; max-width: 45px"
          class="profile-image"
        />
        <div class="column q-px-lg full-width">
          <span class="text-subtitle2 text-weight-bold">
            New user registered.
          </span>
          <span class="text-weight-light text-caption"
            >Won the monthly best seller badge</span
          >
          <span class="text-weight-thin">Yesterday</span>
        </div>
        <div class="column justify-between items-center">
          <q-btn
            icon="close"
            flat
            size="sm"
            class="notification-close-button q-px-sm"
          />
        </div>
      </div>
      <q-btn label="View call notifications" class="full-width" />
    </div>
  </q-menu>
</template>
<script setup></script>
