<template>
  <Menu @pagina-menu="pagina"/>
  <Paginas v-bind:links='links'/>
</template>

<script>
import Paginas from './paginas/paginas.vue'
import Menu from './components/Menu.vue'

export default {
  name: 'App',
  components: {
    Paginas,
    Menu
  },
  data(){
    return{
      links: {
        links:"",
        default:"texto"
      }
    }
  },
  methods:{
    pagina(link){
      this.links.links = link.link
    }
  }
}
</script>
