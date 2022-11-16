<template>
  <div>
    <TestComponent/>
    <Header/>
    <TourInfo/>
    <TourAbout/>
    <OnlinePayment/>
    <Footer/>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  components: 'Header,Tours ',
}
</script>

<style>
@import url(../styles/main.scss);
</style>
