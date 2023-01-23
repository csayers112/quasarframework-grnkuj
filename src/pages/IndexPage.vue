<template>
  <q-page class="column flex-center">
    <div id="q-app" style="min-height: 100vh">
        <div class="row justify-center">
          <div class="col-md-6 col-lg-6 col-xs-12 col-sm-12">
            <div class="top-image"></div>
          </div>
        
          <div class="col-md-6 col-lg-6 col-xs-12 col-sm-12 top-image">
            <div class="q-pa-md content">
              <div class="col-md-9 col-lg-9 col-xl-10 col-sm-12 col-xs-12">
                  <p class="eyebrow-text">WELCOME TO BETTER</p>
                  <h1 class="main-headline">Let’s get you up and running.</h1>
                  <p style="font-size: 20px;">We promised you simple. Now we prove it.</p>
                  <p>Start by talking with your contractor adviser.</p>

                  <button class="q-btn q-btn-item non-selectable no-outline q-btn--standard q-btn--rectangle bg-secondary text-white q-btn--actionable q-focusable q-hoverable full-width" tabindex="0" type="button"><span class="q-focus-helper"></span><span class="q-btn__content text-center col items-center q-anchor--skip justify-center row"><i class="q-icon on-left notranslate material-icons" aria-hidden="true" role="img">calendar</i><span class="block">Talk to us</span></span></button>


              </div>
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
