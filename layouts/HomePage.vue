<template>
  <v-app dark>
    <v-navigation-drawer v-model='drawer' fixed app right>
      <v-list>
        <v-list-item v-for='(item, i) in items' :key='i' :to='item.to' router exact>
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text='item.title' />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-system-bar fixed app color='#0052CC'>
<!--      <v-app-bar-nav-icon class='text-white' @click.stop='drawer = !drawer' />-->
      <v-spacer></v-spacer>
      <div class='text-white'> {{ getTime }}</div>
    </v-system-bar>
    <v-content style='background-color: #0052CC'>
      <nuxt />
    </v-content>
    <Footer />
  </v-app>
</template>
<script lang='ts'>
import { Vue, Component, Prop, Watch, Emit, Ref } from 'vue-property-decorator'
import Footer from '@/components/Layouts/HomePage/Footer.vue'

@Component({
  components: {
    Footer
  },
  computed: {
    getTime() {
      const date = new Date();
      const Hours = date.getHours() < 10 ? "0" + date.getHours().toString(): date.getHours().toString()  ;
      const Minutes = date.getMinutes() < 10 ? "0" + date.getMinutes().toString(): date.getMinutes().toString();
      const Seconds = date.getSeconds()< 10 ? "0" + date.getSeconds().toString(): date.getSeconds().toString();
      return Hours + ":" + Minutes + ":" + Seconds;
    }
  }
})
export default class HomePageLayout extends Vue {
  user = {
    firstName: 'آرمین',
    lastName: 'خیرخواهان'
  }
  clipped = false
  drawer = false
  fixed = false
  items = [
    {
      icon: 'mdi-apps',
      title: 'Welcome',
      to: '/'
    },
    {
      icon: 'mdi-chart-bubble',
      title: 'Inspire',
      to: '/inspire'
    }
  ]
  miniVariant = false
  right = true
  rightDrawer = false
  title = 'Vuetify.js'
}
</script>

<style>
.text-white {
  color: white !important;
}
</style>
