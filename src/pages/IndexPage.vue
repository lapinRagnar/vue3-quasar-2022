<template>

  <q-page class="row">

    <q-card
      class="col-xs-9"
    >
      <q-toolbar class="bg-amber-6">
        <q-input
          class="full-width"
          :model-value="search"
          borderless
          placeholder="rechercher"
          dense
        >

          <template #append>
            <q-icon name="mdi-magnify"></q-icon>
          </template>

        </q-input>


      </q-toolbar>

      <q-list bordered>
        <q-item>

          <q-item-section side>
            <q-checkbox :model-value="true"/>
          </q-item-section>

          <q-item-section>
            faire les course!
          </q-item-section>

          <q-item-section side>
            <q-btn
              flat
              icon="mdi-delete"
              round
              size="sm"
              />
          </q-item-section>


        </q-item>
      </q-list>

    </q-card>

    <div class="col-xs-3">

      <q-toolbar class="bg-teal-6">

        <q-btn
          icon="mdi-plus"
          fab
          color="secondary"
          style="margin-bottom: -45px;"
          class="q-ml-md"
        />

      </q-toolbar>

    </div>


  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import { colors } from 'quasar'

const { getPaletteColor } = colors

export default defineComponent({
  name: "IndexPage",
  data(){
    return {
      search: ''
    }
  },
  mounted(){
    console.log(getPaletteColor('blue'))
  }
});
</script>
