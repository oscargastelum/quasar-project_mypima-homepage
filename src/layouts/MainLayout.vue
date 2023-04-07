<template>
  <q-layout view="lHr lpR fFf">
    <q-header elevated class="bg-white text-black">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />

        <q-toolbar-title class="text-weight-bold">
          <!-- (Commented out avatar logo)
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" />
          </q-avatar>
          -->
          <span class="gt-sm">{{ $route.name }}</span>

          <q-icon
            class="header-icon q-pa-md lt-md"
            name="fa-solid fa-sun"
            size="sm"
            color="primary"
          />
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer
      show-if-above
      v-model="leftDrawerOpen"
      side="left"
      :width="283"
      bordered
    >
      <!-- drawer content -->

      <q-icon
        class="q-pa-md"
        name="fa-solid fa-sun"
        size="lg"
        color="primary"
      />
      <q-list>
        <q-item to="/" clickable exact v-ripple>
          <q-item-section avatar>
            <q-icon name="home" size="md" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold">Home</q-item-section>
        </q-item>

        <q-item to="/NewStudents" clickable exact v-ripple>
          <q-item-section avatar>
            <q-icon name="fa-solid fa-user" size="md" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >New Students</q-item-section
          >
        </q-item>

        <q-item clickable exact v-ripple>
          <q-item-section avatar>
            <q-icon name="fa-solid fa-user-graduate" size="md" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >Students</q-item-section
          >
        </q-item>

        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon name="fa-solid fa-book" size="md" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >Library</q-item-section
          >
        </q-item>

        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon name="fa-solid fa-chalkboard-user" size="md" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >My Courses</q-item-section
          >
        </q-item>

        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon name="fa-solid fa-users" size="md" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >My Communities</q-item-section
          >
        </q-item>
      </q-list>
    </q-drawer>

    <q-drawer show-if-above v-model="rightDrawerOpen" side="right" bordered>
      <!-- drawer content -->

      <q-input
        placeholder="Search MyPima"
        class="q-ma-md"
        outlined
        rounded
        dense
      >
        <template v-slot:prepend>
          <q-icon name="search" />
        </template>
      </q-input>

      <q-list separator padding>
        <q-item class="q-pa-md">
          <q-item-section>
            <q-item-label overline class="text-grey">Graduation</q-item-label>
            <q-item-label class="text-weight-bold"
              >Notice: Graduating Vets & Military-Connected
              Students</q-item-label
            >
            <q-item-label caption>
              Important notice just in! Check your inbox for details and take
              the next step towards your bright future!🇺🇸 #veterans #military
              #education #graduation</q-item-label
            >
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>5 min ago</q-item-label>
          </q-item-section>
        </q-item>

        <q-item class="q-pa-md">
          <q-item-section>
            <q-item-label overline class="text-grey">PCC Alert</q-item-label>
            <q-item-label class="text-weight-bold"
              >Statement From Chancellor Lambert On The Michigan State
              University Shooting
            </q-item-label>
            <q-item-label caption>
              In the wake of last night's shooting at Michigan State University,
              which left three students dead and five others critically
              wounded...</q-item-label
            >
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>30 min ago</q-item-label>
          </q-item-section>
        </q-item>

        <q-item class="q-pa-md">
          <q-item-section>
            <q-item-label overline class="text-grey">Graduation</q-item-label>
            <q-item-label class="text-weight-bold"
              >Complete your FAFSA today
            </q-item-label>
            <q-item-label caption>
              Use Federal School Code 007266 to add Pima Community College.
              Financial aid applications are processing for the following
              academic years...</q-item-label
            >
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>43 min ago</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>

      <q-list class="avatar-list">
        <q-item clickable v-ripple>
          <q-item-section>MyPima</q-item-section>
          <q-item-section avatar>
            <q-avatar color="primary" text-color="white" icon="person" />
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const leftDrawerOpen = ref(false);
    const rightDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },

      rightDrawerOpen,
      toggleRightDrawer() {
        rightDrawerOpen.value = !rightDrawerOpen.value;
      },
    };
  },
};
</script>

<style lang="sass">
.header-icon
  position: absolute
  bottom: 0
  left: 50%
  transform: translate(-50%)


.avatar-list
  position: absolute
  bottom: 16px
  right: 16px
  padding: 8px


@media only screen and (max-width: 768px)
  .avatar-list
    bottom: 32px
    right: 32px



@media only screen and (max-width: 576px)
  .avatar-list
    bottom: 64px
    right: 64px
</style>
