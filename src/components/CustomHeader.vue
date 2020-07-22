<template>
  <header>
    <main-nav/> 
    <secondary-nav/>   
    <div class="head-panel">
      <img src="@/assets/main-image.jpg" class="background-main">
      <div class="info-main">
        <img src="@/assets/logo.png" class="main-logo">  
        <h3>Cooporacion Unificada Nacional de Educacion Superior</h3>
        <button class="btn btn-main">Conocenos</button>
      </div>
    </div>
  </header>
</template>

<script>
import MainNav from '@/components/MainNav'
import SecondaryNav from '@/components/SecondaryNav'

export default {
  name: 'CustomHeader',
  components: {
    MainNav,
    SecondaryNav
  }
}
</script>

<style scoped>
.head-panel {
  display: grid;
  height: 75vh;
  place-content: center;
}
.background-main {
  width: 100vw;
  height: 100%;
  object-fit: cover;
  position: relative;
}
.info-main {
  display: grid;
  background-color: #201f1fab;
  position: absolute;  
  color: white;
  width: 25vw;
  padding: 25px;
  border-radius: 5px;
  top: 150px;
  place-self: center;
  place-items: center;
}
.btn-main {
  color: snow;
  background-color: #82BC00;
}
</style>
