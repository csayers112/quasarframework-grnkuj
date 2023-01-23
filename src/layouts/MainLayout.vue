<template>
  <q-layout>
    <q-header elevated>
      <q-toolbar>
       
        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

   

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>


