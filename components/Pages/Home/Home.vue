<template>
  <div class='items'>
    <img class='avatar elevation-6' src='~/assets/image/person.jpg'>
    <div class='ma-6 welcome'>سلام جهاد</div>
    <v-card class='medal-card'>
      <v-card-text class='pa-3'>
        <Medal class='medal-icon'></Medal>
        <div class='mr-6'>شما استارتر هستید</div>
      </v-card-text>
    </v-card>
    <div class='px-6 pb-7'>
      <HomeItems></HomeItems>
    </div>
  </div>
</template>
<script>
import { Component, Vue } from 'vue-property-decorator'
import HomeItems from '@/components/Pages/Home/HomeItems.vue'
import Medal from '@/assets/svg/medal.svg?inline'

@Component({
  components: { HomeItems, Medal }
})
export default class Home extends Vue {

}
</script>
<style scoped lang='scss'>
.items {
  margin-top: 8rem;
  position: relative;
  padding-top: 4rem;
  background: #FAFAFA 0% 0% no-repeat padding-box;
  box-shadow: 0px -6px 39px #00000061;
  border-radius: 40% 40% 10px 10px;
  opacity: 1;
}

.medal-card {
  width: fit-content;
  margin: 3rem auto;
  padding: 0.5rem;
  div {
    font-weight: bold;
    font-size: 1.1rem;
  }
}

.avatar {
  position: absolute;
  top: -50px;
  left: 0;
  right: 0;
  border: 5px solid white;
  margin-left: auto;
  margin-right: auto;
  width: 100px;
  height: 100px;
  border-radius: 10px;
}

.welcome {
  font-weight: bolder;
  font-size: 1.5rem;
  text-align: center;
}

.medal-icon {
  position: absolute;
  top: -10px;
  right: 0;
}
</style>
