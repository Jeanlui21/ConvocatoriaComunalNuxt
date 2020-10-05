<template lang="html">
  <div>
    <nav class="navbar navbar-expand-lg navbar-light bg-light d-flex align-items-start">
      <div class="row mx-0 w-100">
        <div class="col-12 logo-row d-flex align-items-center">
          <img alt="comunal-logo" height="40" src="~/assets/images/logo.png" width="40">
        </div>
        <div class="col-12 user-row d-flex flex-column justify-content-center">
          <span class="fz-22 font-weight-bolder">Mis problemas</span>
          <div class="d-flex align-items-center">
            <span class="fz-16 font-weight-light text-primary">Problemas</span>
            <span class="fz-22 mx-2 text-black-50">></span>
            <span class="fz-16">Mis problemas</span>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'navbar',
}
</script>

<style scoped lang="css">
nav {
  max-height: 156px;
  min-height: 156px;
  padding: 0;
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
}

.col-12 {
  padding-left: 195px;
  padding-right: 195px;
}

.logo-row {
  height: 64px;
  max-height: 64px;
  box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.1);
}

.user-row {
  height: 91px;
  max-height: 91px;
}
</style>
