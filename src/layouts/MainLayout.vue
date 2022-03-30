<template>
  <q-layout class="hue" view="lHh Lpr lFf">
    <div class="nav container">

      <div class="logo text-h5 q-ml-xl">
      <span class="text-primary text-bold">ONE</span>FIVE
      </div>

      <nav>
        <ul>
          <q-tabs active-color="primary">
            <q-route-tab to="/" label="Home" />
            <q-route-tab class="text-" to="/page2" label="About Us" />
            <q-route-tab class="text-" to="/page3" label="services" />
            <q-route-tab class="text-" to="/page3" label="Contact Us" />

          </q-tabs>
        </ul>
      </nav>

      <nav>
        <ul>
          <q-tabs>
            <q-route-tab class="text-info info text-primary" to="/page1" label="Log in" />
            <q-route-tab class="text-white white bg-primary q-px-lg q-py-sm q-mr-xl" to="/page2" label="Sign Up" />
          </q-tabs>
        </ul>
      </nav>

      <q-btn
          flat
          dense
          class="hide"
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
      />
      <q-drawer
      side="right"
      v-model="leftDrawerOpen"
      bordered
      :breakpoint="1208"
      >
        <q-list>
          <q-item-label
          header
        >
          Essential Links
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
        </q-list>
      </q-drawer>

    </div>


    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksList = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  },
  {
    title: 'Github',
    caption: 'github.com/quasarframework',
    icon: 'code',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Discord Chat Channel',
    caption: 'chat.quasar.dev',
    icon: 'chat',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Forum',
    caption: 'forum.quasar.dev',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Twitter',
    caption: '@quasarframework',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Facebook',
    caption: '@QuasarFramework',
    icon: 'public',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Quasar Awesome',
    caption: 'Community Quasar projects',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev'
  }
];

import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>

<style scoped>

.q-tab__indicator {
    background: #FED12E !important;
}
.q-drawer-container{
  display: none;
}
.hue{
    box-shadow: -1px 0 4px hsl(190, 64%, 15%, 0.15);

}
  .nav{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 70px;

  }

  .hide{
    display: none;
  }

  @media(max-width:768px){
    .hide{
    display: block;
    position: absolute;
    /* top: 1px; */
    z-index: 1000;
    right: 20px;
  }

  .q-drawer-container{
  display: block;
}

  nav{
    display: none;
  }
  }
</style>
