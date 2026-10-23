<script>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import FeaturedProducts from './components/FeaturedProducts.vue'
import Footer from './components/Footer.vue'
import Products from './components/Products.vue';

export default{
  components:{
    Navbar,
    Home,
    FeaturedProducts,
    Products,
    Footer
  },
  data(){
    return{
      currentPage: 'Home',
    }
  },
  methods:{
    navi(i){
      this.currentPage = i;
    }
  }
}
</script>

<template>
  <Navbar @goTo="navi" />
  <Home v-if="currentPage === 'Home'" />
  <FeaturedProducts  />
  <Products v-if="currentPage === 'Products'" />
  <Footer />
</template>
