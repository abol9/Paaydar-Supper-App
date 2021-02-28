<template>
  <v-row>
    <v-col cols='4' sm='4' v-for='item of items' style='padding: 3px'>
      <v-card outlined tile class='elevation-7 rounded-xl'>
        <v-card-text class='text-center'>
          <component :is='item.icon'/>
          <div class='mt-4 text-center menu-title'> {{ item.title }}</div>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script lang='ts'>
import { Vue, Component, Prop, Watch, Emit, Ref } from 'vue-property-decorator'
import Discount from '@/assets/svg/discount.svg?inline';
import User from '@/assets/svg/user.svg?inline';
import DesignBook from '@/assets/svg/design-book.svg?inline';
import Cont from '@/assets/svg/content.svg?inline';
import Summer from '@/assets/svg/summer.svg?inline';
import Scatter from '@/assets/svg/scatter.svg?inline';
import Graph from '@/assets/svg/graph.svg?inline';
import Portfolio from '@/assets/svg/portfolio.svg?inline';
import Juice from '@/assets/svg/juice.svg?inline';
@Component({
  components: {
    Discount,
    User,
    Cont,
    DesignBook,
    Scatter,
    Graph,
    Portfolio,
    Juice,
    Summer
  }
})
export default class Menu extends Vue {
  items: any = [
    { icon: 'discount', title: 'پاوینتو' },
    { icon: 'user', title: 'متخصصین' },
    { icon: 'design-book', title: 'سفیران' },
    { icon: 'cont', title: 'آموزش' },
    { icon: 'summer', title: 'بیمه' },
    { icon: 'graph', title: 'سهام' },
    { icon: 'juice', title: 'گردشگری' },
    { icon: 'scatter', title: 'ابزارها' },
    { icon: 'portfolio', title: 'خدمات' }
  ]
}
</script>
<style scoped>
.menu-title {
  font-size: 12px;
  font-weight: bold;
}


.text-center {
  text-align: center;
}
</style>
