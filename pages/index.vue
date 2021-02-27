<style lang="scss" scoped>
.home {
  background-color: #0052CC;
  border-radius: 10px;
}
</style>
<template>
  <div class='home'>
    <TopHeader />
    <Home>
    </Home>
  </div>
</template>
<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator'
Component.registerHooks(['fetch'])
import TopHeader from '@/components/Pages/Home/TopHeader.vue'
import Home from '@/components/Pages/Home/Home.vue'
import HomeItems from '@/components/Pages/Home/HomeItems.vue'
@Component({
  layout: 'HomePage',
  components: {
    HomeItems,
    TopHeader,
    Home
  }
})
export default class HomePage extends Vue {}
</script>

