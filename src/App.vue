

<template>
  <div class="corpo"> 

    <meu-menu :rotas="routes"></meu-menu>

      <Transition name="pagina">
        <router-view></router-view>
      </Transition>

  </div>
</template>

<script>
import { routes } from './routes';
import Menu from './components/shared/menu/Menu.vue'

export default {

  components: {
    'meu-menu' : Menu

  },

  data() {

    return {

      routes
    }
  }
}

</script>

<style>

.corpo {
  font-family: Helvetica, sans-serif;
  width: 96%;
  margin: 0 auto;
}

.menu {
  font-family: Helvetica, sans-serif;
    
}

.pagina-enter-active, .pagina-leave-active {

  transition: opacity .1s;
}

</style>
