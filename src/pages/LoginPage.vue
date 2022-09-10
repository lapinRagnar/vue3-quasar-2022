<template>
  <q-page class="flex flex-center" padding>

    <div class="full-width mon-card">

      <h5 class="q-my-md text-center full-width">Login</h5>

      <q-card class="full-width ">

        <q-card-section>

          <q-form>

            <q-input label="email" placeholder="email@example.com" class="q-mb-md" />

            <q-input label="password" type="password" class="q-mb-md"/>

            <q-checkbox :model-value="true" label="se rappeler" />

            <q-btn label="se connecter" color="teal-6" class="full-width" />

          </q-form>



        </q-card-section>

    </q-card>

    </div>

  </q-page>
</template>

<script>
export default {
  name: 'LoginPage',
}
</script>

<style scoped>

  .mon-card {
    max-width: 400px;
  }
</style>

