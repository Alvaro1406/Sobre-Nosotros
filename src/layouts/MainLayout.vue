<template>
  <q-layout view="hhh lpR fff" class="bg-primary">
    <q-header class="bg-primary text-white">
      <sobre-nosotros4 />
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer class="text-white q-pt-xl">
      <div class="row justify-center q-pa-md">
        <div class="col-10 col-sm-4 col-md-2 q-pl-md flex flex-center"><SobreNosotros6 /></div>
        <div class="col-10 col-sm-4 col-md-3 q-pl-md"><SobreNosotros5 /></div>
        <div class="col-10 col-sm-4 col-md-2 q-pl-md"><SobreNosotros7 /></div>
        <div class="col-10 col-sm-4 col-md-3 q-pl-md"><SobreNosotros8 /></div>
        <img
          alt="Quasar logo"
          src="~assets/footer.png"
          class="absolute-right q-pt-xl"
          style="width: 1000px; height: 1000px"
        />
      </div>
      <SobreNosotros9 />
    </q-footer>
  </q-layout>
</template>

<script>
import SobreNosotros4 from 'src/components/SobreNosotros4.vue'
import SobreNosotros5 from 'src/components/SobreNosotros5.vue'
import SobreNosotros6 from 'src/components/SobreNosotros6.vue'
import SobreNosotros7 from 'src/components/SobreNosotros7.vue'
import SobreNosotros8 from 'src/components/SobreNosotros8.vue'
import SobreNosotros9 from 'src/components/SobreNosotros9.vue'
export default {
  components: { SobreNosotros4, SobreNosotros5, SobreNosotros6, SobreNosotros7, SobreNosotros8, SobreNosotros9 }
}
</script>
