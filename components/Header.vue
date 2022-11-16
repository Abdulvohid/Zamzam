<script>
export default {
  name: 'HedaerComponent',
  components: 'LangButton, Tours ',

  data() {
    return {
      close: false,
      open: true,
    }
  },

  methods: {
    closeButton() {
      this.close = false
      console.log('closebutton ishladi')
    },
    openButton() {
      this.close = true
    },
  },
}
</script>

<template>
  <div class="hero">
    <div class="hero_bg">
      <div class="container">
        <header>
          <div class="logo">
            <a href="/">
              <img src="../assets/images/logo.png" alt="" />
            </a>
          </div>
          <nav class="nav">
            <ul>
              <li>
                <a href="tel:+998916191900">+998916191900</a>
              </li>
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
            <LangButton />
          </nav>
          <div class="mobile-menu" v-if="close">
            <button class="mobile-button" @click="closeButton()">
              <svg
                width="25px"
                height="25px"
                viewBox="0 0 512 512"
                xmlns="http://www.w3.org/2000/svg"
              >
                <polygon
                  fill="#fff"
                  points="427.314 107.313 404.686 84.687 256 233.373 107.314 84.687 84.686 107.313 233.373 256 84.686 404.687 107.314 427.313 256 278.627 404.686 427.313 427.314 404.687 278.627 256 427.314 107.313"
                  class="ci-primary"
                />
              </svg>
            </button>
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
              <li>
                <a href="tel:+998916191900">+998916191900</a>
              </li>
            </ul>
          </div>
          <div style="display:flex">
            <LangButton />
            <button class="hamburger" v-if="open" @click="openButton()">
              <svg
                width="40px"
                height="40px"
                viewBox="0 0 72 72"
                id="emoji"
                xmlns="http://www.w3.org/2000/svg"
              >
                <g id="color" />
                <g id="hair" />
                <g id="skin" />
                <g id="skin-shadow" />
                <g id="line">
                  <line
                    x1="16"
                    x2="56"
                    y1="26"
                    y2="26"
                    fill="none"
                    stroke="#000000"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-miterlimit="10"
                    stroke-width="2"
                  />
                  <line
                    x1="16"
                    x2="56"
                    y1="36"
                    y2="36"
                    fill="none"
                    stroke="#000000"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-miterlimit="10"
                    stroke-width="2"
                  />
                  <line
                    x1="16"
                    x2="56"
                    y1="46"
                    y2="46"
                    fill="none"
                    stroke="#000000"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-miterlimit="10"
                    stroke-width="2"
                  />
                </g>
              </svg>
            </button>
          </div>
        </header>

        <Tours />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.hero {
  background-image: url('../assets/images/banner.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-blend-mode: luminosity;
  width: 100%;
  height: 100vh;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #11795f;
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
      font-size: 16px;
      transition: 0.5s;

      &:hover {
        border-bottom: 1px solid #11795f;
        transition: 0.5s;
      }

      a {
        color: #11795f;
        text-decoration: none;
      }
    }
    a {
      color: #11795f;
      text-decoration: none;
    }
  }
}
.main-title {
  h2 {
    color: #11795f;
    margin: 0 auto;
    text-align: center;
    font-size: 48px;
    margin-top: 120px;
  }
  button {
    // margin: 0 auto;
    // display: flex;
    background: #11795f;
    border-radius: 60%;
    border-color: #11795f;
    padding: 14px 10px 14px 10px;
    cursor: pointer;
    margin-top: 25px;
    color: #fff;
    border: none;
    width: 120px;
    height: 60px;
    text-align: center !important;

    &:hover {
      background-color: #0c5543;
      color: #fff;
      border: none;
    }
  }
}

.hamburger {
  display: none;
}

@media only screen and (max-width: 425px) {
  .container {
    padding: 0;
  }
  .nav {
    display: none;
  }

  .hamburger {
    display: block;
    background: transparent;
    border: none;
  }

  .mobile-menu {
    display: flex;
    width: 100%;
    height: 100%;
    background: #11795f;
    position: fixed;
    color: #fff;
    z-index: 100;
    top: 0;
    justify-content: end;

    ul {
      text-align: center;
      color: #fff;
      display: flex;
      flex-direction: column;
      margin: 0 auto;
      margin-top: 116px;
      li {
        display: flex;
        flex-direction: column;
        color: #fff;
        margin-bottom: 20px;
        a {
          color: #fff;
        }
      }
    }
  }

  .mobile-button {
    background: transparent;
    border: none;
    right: 16px;
    top: 10px;
    display: flex;
    justify-content: center;
    position: absolute;
  }
}
</style>
