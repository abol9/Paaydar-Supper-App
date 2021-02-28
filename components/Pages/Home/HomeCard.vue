<template>
  <v-card color='#46286F' class='elevation-5 ma-1 mt-5 rounded-lg home-card'>
    <img src='@/assets/image/card.png' class='card-image'>
    <div class='title'>
      پایدار کارت
    </div>
    <div class='subtitle'>
      مشاهده جزئیات
    </div>
    <Arrow class='arrow'></Arrow>
  </v-card>
</template>
<script>
import {Component, Vue} from 'vue-property-decorator';
import Arrow from '@/assets/svg/arrow.svg?inline';
@Component({
  components: {
    Arrow
  }
})
export default class HomeCard extends Vue {

}
</script>
<style lang='scss'>
.card-image {
  margin-top: -20px !important;
  float: right;
}

.home-card {
  min-height: 100px ;
}
.title {
  color: white;
  text-align: center;
  padding-left: 2rem;
  padding-top: 2rem;
}
.subtitle {
  color: #ccc;
  font-size: 0.8rem;
  text-align: center;
  padding-left: 2rem;
}
.arrow {
  background-color: white;
  border-radius: 50%;
  position: absolute;
  left: 20px;
  top: 0;
  bottom: 0;
  margin-top: auto;
  margin-bottom: auto;
}
</style>
