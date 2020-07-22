<template>
  <nav class="navbar navbar-expand-lg navbar-ligth bg-ligth secondary-nav">
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navegationMenuSecondary" aria-controls="navegationMenu" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon">CUN</span>
  </button>
  <div class="collapse navbar-collapse" id="navegationMenuSecondary">
    <ul class="navbar-nav">
      <li class="nav-item nav-secondary-item" v-for="(item, index) in items" v-bind:key="index">
        <a class="nav-link" v-if="item.url" v-bind:href="item.url">{{ item.name }}</a>
      </li>         
    </ul>        
 </div>
  </nav>
</template>

<script>
export default {
  name: 'SecondaryNav',
  data() {
    return {
      items: [
        {name: 'Estudiantes', url:'/'},
        {name: 'Transferencias', url: '/'},
        {name: 'Biblioteca', url: '/'},
        {name: 'Internacionalizacion', url: '/'},
        {name: 'Practicas', url: '/'},
        {name: 'Bienestar', url: '/'},
        {name: 'Grado', url: '/'}
      ]
    }
  }
}
</script>

<style scoped>
.secondary-nav {
  display: grid;
  place-content : center;
  padding-top: 66px;
  padding-bottom: unset;
}
.nav-link {
  color: black;
}
.nav-link:hover {
  color: #82BC00;
}
.nav-secondary-item:hover {
  border-top: 4px solid #82BC00;
}
</style>
