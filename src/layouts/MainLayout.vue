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

        <TodosList/>

      </q-list>
    </q-drawer>

    <q-page-container>

      <router-view />

    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import TodosList from 'src/components/TodosList.vue'



export default defineComponent({
  name: 'MainLayout',

  components: {
    TodosList
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
