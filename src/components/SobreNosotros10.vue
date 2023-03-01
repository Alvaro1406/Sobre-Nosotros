<template>
  <q-table
    class="q-mt-md"
    title="Componentes"
    no-data-label="No hay componentes q mostrar."
    :columns="columns"
    :rows="componentes"
  />
</template>

<script>
const columns = [
  {
    name: 'componente',
    label: 'Componente',
    align: 'left',
    field: 'componente',
    sortable: true
  },
  {
    name: 'estado',
    label: 'Estado',
    align: 'left',
    field: 'estado',
    sortable: true
  }
]

const rows = [
  {
    componente: 'producto1',
    estado: 'Excelente'
  }
]

export default {
  props: {
    componentes: Array
  },
  setup () {
    return {
      columns,
      rows
    }
  }
}
</script>
