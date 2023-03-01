<template>
  <q-page padding class="bg-white">
    <h4 class="text-secondary">Agregar Componentes de PC</h4>
    <pre>{{ componente }} - {{estado}} - {{terminos}}</pre>
    <q-form
    class="row q-col-gutter-md"
    @submit.prevent="procesarFormulario"
    @reset="reset"
    ref="myForm"
    >
      <div class="col-12 col-sm-6">
        <q-input
        label="Componente"
        v-model="componente"
        :rules="[ val => val && val.length > 0 || 'Por favor escriba algo']"
        lazy-rules/>
      </div>
      <div class="col-12 col-sm-6">
        <q-select
        label="Estado"
        v-model="estado"
        :options="opciones"
        :rules="[ val => val && val.length > 0 || 'Por favor escriba algo']"
        lazy-rules/>
      </div>
      <div class="col-12">
      <q-toggle
      label="Aceptar los terminos"
      v-model="terminos"
      />
      </div>
      <div class="col-12">
      <q-btn color="secondary" label="Submit" type="submit" />
        <q-btn
          label="Reset"
          color="secondary"
          outline
          class="q-ml-sm"
          :ripple="false"
          type="reset"
        />
      </div>
    </q-form>
    <SobreNosotros10 :componentes="componentes"/>
  </q-page>
</template>

<script>
import { ref } from 'vue'
import { useQuasar } from 'quasar'
import SobreNosotros10 from 'src/components/SobreNosotros10.vue'
export default {
  components: { SobreNosotros10 },
  setup () {
    const $q = useQuasar()
    const myForm = ref(null)
    const componente = ref()
    const estado = ref()
    const terminos = ref(false)
    const opciones = ['excelente', 'bueno', 'malo']

    const componentes = ref([])

    const procesarFormulario = () => {
      console.log('me diste click al formulario')
      if (terminos.value === false) {
        $q.notify({
          color: 'red-5',
          textColor: 'white',
          icon: 'warning',
          message: 'Acepte los terminos antes de continuar.'
        })
      } else {
        $q.notify({
          color: 'green-4',
          textColor: 'white',
          icon: 'cloud_done',
          message: 'Insertado correctamente'
        })

        myForm.value.resetValidation()
        componentes.value = [...componentes.value, {
          componente: componente.value,
          estado: estado.value
        }]

        reset()
      }
    }

    const reset = () => {
      componente.value = null
      estado.value = null
      terminos.value = false
    }

    return {
      componente,
      estado,
      opciones,
      procesarFormulario,
      terminos,
      reset,
      myForm,
      componentes
    }
  }
}
</script>
