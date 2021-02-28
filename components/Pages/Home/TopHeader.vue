<style lang="scss" scoped>
</style>
<template>
  <div class='text-center pt-6'>
    <Logo style='width: 70px;' />
    <div class='logo-title mt-4'>شهر هوشمند پایدار</div>
  </div>
</template>
<script lang="ts">
import { Vue, Component, Prop, Watch, Emit, Ref } from 'vue-property-decorator'
import Logo from '@/assets/svg/logo.svg?inline'
@Component({
  components: {
    Logo
  }
})
export default class TopHeader extends Vue {}
</script>
<style>
.logo-title {
  font-size: 1.5rem;
  font-weight: bolder;
  color: white;
}
</style>
