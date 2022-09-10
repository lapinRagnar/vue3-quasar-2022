<template>
  <q-layout view="hHh Lpr lFf">
    <q-header>
      <q-toolbar class="bg-teal-6" >
        <q-btn
          flat
          dense
          round
          icon="mdi-menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>

        <q-btn
          icon="mdi-logout"
          flat
          round
        />
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>

        <q-toolbar class="bg-teal-6" />

        <q-item class="bg-purple-2">
          <q-item-section>
            lists
          </q-item-section>

          <q-item-section side>
            <q-btn
              icon="mdi-plus"
              flat
              round
              size="sm"

            />
          </q-item-section>
        </q-item>

        <q-item clickable>

          <q-item-section side>
            <q-icon name="mdi-shopping" />
          </q-item-section>

          <q-item-section class="text-red">
            liste des courses
          </q-item-section>

          <q-item-section side>
            2
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
import { defineComponent, ref } from 'vue'



export default defineComponent({
  name: 'MainLayout',

  components: {

  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {

      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
