<template>
    <div class="container">
       <Header></Header>
       <Body></Body>
       <Footer></Footer>
       
    </div>
</template>

<script>
import Body from './children/Body.vue'
import Footer from './children/Footer.vue'
import Header from './children/Header'


export default {
  components: { Header,Body,Footer},
  
}
    
</script>

<style scoped>
.container{
    width: 100%;
    
    background:url(../../image/beijing.png);
}
</style>
