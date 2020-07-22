<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark navbar-main">
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navegationMenu" aria-controls="navegationMenu" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    
    <div class="collapse navbar-collapse " id="navegationMenu">
      <a class="navbar-brand" href="#">
        <img src="@/assets/favicon.png" class="img-logo">  
      </a>
      <div class="navbar-nav mr-auto mt-2 mt-lg-0"></div>
      <ul class="navbar-nav my-2 my-lg-0">
        <li class="nav-item" v-for="(item, index) in items" v-bind:key="index">
          <a class="nav-link" v-if="item.url" v-bind:href="item.url">{{ item.name }}</a>
          <a class="nav-link" v-if="!item.url" data-toggle="modal" data-target="#signinModal">{{ item.name }}</a>
        </li>         
      </ul>        
   </div>
  </nav>
</template>

<script>
export default {
  name: 'MainNav',
  data() {
    return {
      items: [
        {name: 'Información', url:'/'},
        {name: 'Sedes', url: '/'},
        {name: 'Programas', url: '/'},
        {name: 'Transferencias', url: '/'},
        {name: 'Contactanos', url: '/'},
      ]
    }
  }
}
</script>

<style scoped>
  .img-logo {
    width: 2em;
  }
  .navbar-main {
    width: 100vw;
    position: fixed;
    z-index: 2;
  }
</style>
