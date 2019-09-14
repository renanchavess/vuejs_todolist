<template>
  <div id="app">
    <Nav></Nav>
    <section class="content-page">
      <Lista/>
    </section>  
    
    
    
    
    
  </div>
</template>

<script>
import Lista from './components/Lista/Lista.vue'
import Nav from './components/_nav/Nav.vue'

export default {
  name: 'app',
  components: {
    Lista,
    Nav
  }
}
</script>

<style>
#app {
  color: rgb(0, 16, 160);
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

.content-page{
  padding:20px;
}
</style>
