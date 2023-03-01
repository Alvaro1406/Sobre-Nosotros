<template>
  <div class="row justify-center">
    <div class="col-12 col-sm-6 col-md-4 col-lg-6 q-pa-xs">
      <img
        src="~assets\LOGO.png"
        style="width: 60px; height: 30px"
        alt=""
        class="q-p-md"
      />
      <q-toolbar inset>
        <q-breadcrumbs active-color="white" style="font-size: 14px">
          <q-breadcrumbs-el
            label="Inicio"
            to="/"
            active-class="my-menu-link"
            exact
          />
          <q-breadcrumbs-el
            label="Conozcanos"
            to="/indexpage2"
            active-class="my-menu-link"
          />
          <q-breadcrumbs-el
            label="Formulario"
            to="/indexpage3"
            active-class="my-menu-link"
          />
        </q-breadcrumbs>
      </q-toolbar>
    </div>
    <div class="col-12 col-sm-6 col-md-6 col-lg-4 q-pa-xs">
      <q-toolbar inset>
        <q-breadcrumbs active-color="white" style="font-size: 12px">
          <img src="~assets\group.png" style="width: 15px; height: 15px" />
          <q-btn text-color="white" label="Administracion" flat size="8px" />
          <q-btn text-color="white" label="Portafolio" flat size="8px" />
          <q-btn text-color="positive" label="Conozcanos" flat size="8px" />
          <q-btn text-color="white" label="Servicios" flat size="8px" />
          <q-btn text-color="white" label="Contacto" flat size="8px" />
          <q-btn text-color="positive" label="Cerrar" outline size="8px" />
        </q-breadcrumbs>
      </q-toolbar>
    </div>
  </div>
</template>

<style lang="scss">
.my-menu-link {
  color: #76bc21;
}
</style>
