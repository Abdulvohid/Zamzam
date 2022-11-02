<script>
export default {
  name: 'footer-component',
}
</script>

<template>
  <footer>
    <div class="container">
      <div class="footer-hero">
        <div class="footer-contact">
          <div class="logo">
            <img src=".././assets/images/logo-footer.png" alt="" />
          </div>
          <p>{{$t('call')}}</p>
          <a href="tel:+998916191900">+998916191900</a>
          <p>{{$t('adres')}}: {{$t('adreestext')}}</p>
        </div>

        <div class="footer_info">
          <ul>
            <li>
              <a href="/"> {{ $t('visa') }}</a>
            </li>
            <li>
              <a href="/"> {{ $t('payment') }}</a>
            </li>
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
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss">
footer {
  background: #11795f;
  font-family: 'poppins';
  font-weight: 400;
  padding: 12px;

  p {
    color: #fff;
  }

  a {
    color: #fff;
    padding-left: 5px;
  }
}

.footer-hero {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

@media only screen and (max-width: 425px) {
    .footer-hero{
        display:flex;
        flex-direction: column;
        text-align: center;
    }
}
</style>
