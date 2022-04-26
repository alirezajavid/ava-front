<template>
  <q-page class="flex flex-center">
    <!-- Now obviously not like this : ) but how ? -->
    <transition appear enter-active-class="animated bounceInDown"
    leave-active-class="animated flipOutY" :duration="2000  0">
      <q-card
        v-show="show"
        style="
        background-color: #FCFFE7;
        width: 600px;
        background: url(/b1.png) no-repeat;
        "
      >
        <div style="text-align:center; margin-top:40px; font-size: 24px; ">
          مرحله اول
        </div>
        <div style="direction:rtl; text-align:right; margin-top:20px; padding: 40px; font-size:18px;">
          سلام آوا عزیز
        </div>
      </q-card>
    </transition>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data() {
    return {
      show: false
    }
  },
  mounted() {
    setTimeout(() => { this.show = !this.show}, 2000)
  }
}
</script>
