<template>
  <q-menu class="header-menu-dropdown">
    <q-list style="min-width: 200px">
      <q-item clickable v-ripple>
        <q-item-section avatar>
          <q-img
            src="../../assets/female.jpg"
            spinner-color="white"
            style="height: 45px; max-width: 45px"
            class="profile-image"
          />
        </q-item-section>

        <q-item-section class="column">
          <span class="text-subtitle2">Anna Mrkvicka</span>
          <span>x</span>
          <span class="text-weight-light text-caption">Admin</span>
        </q-item-section>
      </q-item>

      <q-separator />

      <q-item clickable v-ripple class="q-px-lg">
        <q-item-section avatar>
          <q-avatar icon="person_outline" />
        </q-item-section>
        <q-item-section>Profile</q-item-section>
      </q-item>
      <q-item clickable v-ripple class="q-px-lg">
        <q-item-section avatar>
          <q-avatar icon="payment" />
        </q-item-section>
        <q-item-section>Billing</q-item-section>
      </q-item>

      <q-separator />

      <q-item clickable v-ripple class="q-px-lg">
        <q-item-section avatar>
          <q-avatar icon="logout" />
        </q-item-section>
        <q-item-section>Logout</q-item-section>
      </q-item>
    </q-list>
  </q-menu>
</template>
<script setup></script>
