<template>
  <div class="min-h-screen flex flex-col bg-[rgb(33,43,69)]">
    <Header />
    <div class="flex-1">
      <router-view />
      
    </div>
    <Footer/>
  </div>
</template>
<script>
import Header from '@/components/Header'
import Footer from '@/components/Footer'
  export default{
    components:{
      Header,Footer
    }
  }
</script>
<style>
body{
  font-family: 'Helvetica', sans-serif;
}
</style>
