<template>
  <q-page class="flex flex-center">
    <SobreNosotros />
    <SobreNosotros2 />
    <SobreNosotros3 />
  </q-page>
</template>

<script>
import SobreNosotros from 'src/components/SobreNosotros.vue'
import SobreNosotros2 from 'src/components/SobreNosotros2.vue'
import SobreNosotros3 from 'src/components/SobreNosotros3.vue'
export default {
  components: { SobreNosotros, SobreNosotros2, SobreNosotros3 }
}
</script>
