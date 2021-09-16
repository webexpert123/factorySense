<template>
<div class="bg-white">
  <Header />
  <main>
      <nuxt-child />
  </main>
  <Footer />
 
</div>    
</template>
<script>
import Header from '@/components/common/Header'
import Footer from '@/components/common/Footer'
export default {
    name: 'DefaultLayout',
    components: { Header, Footer }
}
</script>