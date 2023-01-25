<template>
  <q-layout>
    <q-header elevated>
      <q-toolbar class="bg-white">


  

        <div style="padding: 10px">
          <img
            width="100"
            height="40"
            alt="Acorn Finance"
            id="logo"
            src="https://www.acornfinance.com/wp-content/uploads/2021/09/acorn-finance-logo-compressed.svg"
          />
        </div>

        <q-space />


        <q-btn flat color="secondary" label="Talk to us"></q-btn>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>
