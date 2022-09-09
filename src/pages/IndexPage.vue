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
        >

          <template #append>
            <q-icon name="mdi-magnify"></q-icon>
          </template>

        </q-input>


      </q-toolbar>

      <q-list>
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


  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
  data(){
    return {
      search: ''
    }
  }
});
</script>
