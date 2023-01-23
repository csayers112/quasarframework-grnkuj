<template>
  <q-page class="column flex-center">
    <div id="q-app" style="min-height: 100vh">
        <div class="row">
          <div class="col top-image">

          </div>
        </div>
        <div class="q-pa-md">
          <div class="row justify-center">
            <div class="col-md-9 col-lg-9 col-xl-10 col-sm-12 col-xs-12">
              .col-12 .col-md-auto (Variable width content)
            </div>
          </div>
      </div>
    </div>
   
   
  </q-page>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);

const min = -5;
const max = 5;
</script>
