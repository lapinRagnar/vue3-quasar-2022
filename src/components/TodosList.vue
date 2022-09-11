<template>

  <q-list>

    <q-toolbar class="bg-teal-6" />

      <q-item class="bg-purple-2">
        <q-item-section>
          lists
        </q-item-section>


        <q-item-section side>
          <CreateTodoListButton />
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
</template>

<script>
import CreateTodoListButton from './CreateTodoListButton.vue';
export default {
    name: "TodosList",
    setup() {
        return {};
    },
    components: { CreateTodoListButton }
}
</script>
