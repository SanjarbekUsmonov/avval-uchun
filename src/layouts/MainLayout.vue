<template>
  <q-layout view="hHh lpR fff">

    <q-header bordered class="bg-transparent"  height-hint="98"  unelevated>
      <q-toolbar>
        <q-toolbar-title>
          <!-- v-for uchun -->

    <div class="q-pa-md fit row no-wrap justify-around items-center" >
      <div class="logo">
            <span>AVVAL</span>

          </div>
          <div class="button ">
            <q-btn-dropdown color="transparent" unelevated :label="fruit.label" v-for="fruit in fruits" :key="fruit">
      <q-list>
        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label >{{fruit.name1}}</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>{{fruit.video}}</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>{{fruit.artic}}</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-btn-dropdown>
          </div>

    <div class="icon">
      <q-icon name="lock">

       </q-icon>
       <q-icon name="search" class="q-ml-md">

       </q-icon>
    </div>
  </div>
  <div class="icon">

  </div>
        </q-toolbar-title>
      </q-toolbar>


    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar>
          <div>Title</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>
<script>
export default {
  setup () {
    return {
      onItemClick () {
        // console.log('Clicked on an Item')
      },

    }
  },
  data() {
        return {
          fruits:[
            {name1:'Photos',video:'Videos',artic:'Articles',label:'Home'},
            {name1:'Photos',video:'Videos',artic:'Articles',label:'pages'},
            {name1:'Photos',video:'Videos',artic:'Articles',label:'pages'},
            {name1:'Photos',video:'Videos',artic:'Articles',label:'pages'},
            {name1:'Photos',video:'Videos',artic:'Articles',label:'pages'},
            {name1:'Photos',video:'Videos',artic:'Articles',label:'pages'},
            {name1:'Photos',video:'Videos',artic:'Articles',label:'pages'}
          ]
        }
      },
}
</script>
