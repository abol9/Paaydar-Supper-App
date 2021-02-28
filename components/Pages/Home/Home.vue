<template>
  <div class='items pb-2'>
    <BellNotif class='bell-notif'></BellNotif>
    <NotifEllipse class='notif-ellipse'></NotifEllipse>
    <MenuBurger class='menu-burger'></MenuBurger>
    <img class='avatar' src='~/assets/image/person2.png'>
    <div class='welcome'>
      <span>سلام،</span>
      <span class='name'>سارا</span>
    </div>
    <v-card class='medal-card'>
      <v-card-text class='pa-2'>
        <Medal class='medal-icon'></Medal>
        <div class='mr-6'>شما استارتر هستید</div>
      </v-card-text>
    </v-card>
    <div class='px-4 pb-4'>
      <HomeItems></HomeItems>
    </div>
    <HomeCard></HomeCard>
  </div>
</template>
<script>
import { Component, Vue } from 'vue-property-decorator'
import HomeItems from '@/components/Pages/Home/HomeItems.vue'
import Medal from '@/assets/svg/medal.svg?inline'
import HomeCard from '@/components/Pages/Home/HomeCard.vue'
import BellNotif from '@/assets/svg/bell-notifications.svg?inline'
import NotifEllipse from '@/assets/svg/notif-ellipse.svg?inline'
import MenuBurger from '@/assets/svg/menu-burger.svg?inline'
@Component({
  components: {
    HomeItems,
    Medal,
    HomeCard,
    BellNotif,
    NotifEllipse,
    MenuBurger
  }
})
export default class Home extends Vue {

}
</script>
<style scoped lang='scss'>
.items {
  margin-top: 4rem;
  position: relative;
  padding-top: 2rem;
  background: #FAFAFA 0 0 no-repeat padding-box;
  box-shadow: 0px -6px 39px #00000061;
  border-radius: 276px/147px;
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}
.bell-notif {
  position: fixed;
  top: 30px;
  left: 10px;
}

.notif-ellipse {
  position: fixed;
  top: 30px;
  left: 25px;
}

.menu-burger {
  position: fixed;
  top: 30px;
  right: 10px;
}

.medal-card {
  width: fit-content;
  margin: 0.5rem auto 1rem auto;

  div {
    font-weight: bold;
    font-size: 0.8rem;
  }
}

.avatar {
  position: absolute;
  top: -40px;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  width: 72px;
  height: 72px;
}

.welcome {
  text-align: center;
  .name {
    font-weight: bolder;
    font-size: 1.5rem;
  }
}

.medal-icon {
  position: absolute;
  top: -10px;
  right: 0;
}

.container {
  padding: 0;
}
</style>
