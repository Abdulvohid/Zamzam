<script>
export default {
  name: 'HedaerComponent',
  components: 'LangButton',
}
</script>

<template>
  <header>
    <div class="logo">
      <img src="../assets/images/logo.png" alt="" />
    </div>
    <nav>
      <ul>
        <li></li>
        <li>
          <a href="/"> {{ $t('contact') }}</a>
        </li>
        <li>
          <a href="/"> {{ $t('info') }}</a>
        </li>
        <li>

        <NuxtLink to="/about">
          <a href="/"> {{ $t('about') }} </a>
        </NuxtLink>
    </li>

      </ul>
      <LangButton />
    </nav>
  </header>
</template>

<style lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #11795f;
  ul {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 30px;
    padding-right: 15px;
    li {
      display: flex;
      justify-content: space-between;
      align-items: center;
      color: #11795f;
      font-size: 16px;        transition: .5s;


      &:hover{
        border-bottom: 1px solid #11795f;
        transition: .5s;
      }

   
    
      a{
        color: #11795f;
        text-decoration: none;
     
      }
    }
        a{
        color: #11795f;
        text-decoration: none;
      }
    }
}
</style>
