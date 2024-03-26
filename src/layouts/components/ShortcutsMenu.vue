<template>
  <q-menu
    transition-show="jump-down"
    transition-hide="jump-up"
    class="header-menu-dropdown"
  >
    <div>
      <div class="row no-wrap q-pa-md justify-between items-center">
        <span class="text-h6">Shortcuts</span>
        <q-btn icon="grid_view" flat size="sm" />
      </div>
      <q-separator />
      <div class="q-py-md q-px-sm row no-wrap items-center notification-row">
        <q-btn flat dense no-caps class="q-pa-lg">
          <div class="flex column items-center justify-center text-center">
            <q-icon name="calendar_month" class="shortcut-button q-pa-sm" />
            <span class="text-weight-light">Calendar Appointments</span>
          </div>
        </q-btn>
        <q-btn flat dense no-caps class="q-pa-lg">
          <div class="flex column items-center justify-center text-center">
            <q-icon name="insert_drive_file" class="shortcut-button q-pa-sm" />
            <span class="text-weight-light">Invoice App Manage Accounts</span>
          </div>
        </q-btn>
      </div>
      <div class="q-py-md q-px-sm row no-wrap items-center notification-row">
        <q-btn flat dense no-caps class="q-pa-lg">
          <div class="flex column items-center justify-center text-center">
            <q-icon name="calendar_month" class="shortcut-button q-pa-sm" />
            <span class="text-weight-light">Calendar Appointments</span>
          </div>
        </q-btn>
        <q-btn flat dense no-caps class="q-pa-lg">
          <div class="flex column items-center justify-center text-center">
            <q-icon name="insert_drive_file" class="shortcut-button q-pa-sm" />
            <span class="text-weight-light">Invoice App Manage Accounts</span>
          </div>
        </q-btn>
      </div>
    </div>
  </q-menu>
</template>
<script setup></script>
