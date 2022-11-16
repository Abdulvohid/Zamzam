<template>
  <div>
    <h2>{{$t('paymentsystem')}}</h2>
    <div class="cart-image">
      <img src=".././assets/images/payme.png" alt="" />
      <img src=".././assets/images/click.png" alt="" />
      <img src=".././assets/images/visa.png" alt="" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
div {
  margin-top: 48px;
  h2 {
    text-align: center;
    color: #a87d32;
  }
  .cart-image {
    display: flex;
    justify-content: space-evenly;
    margin: 0 auto;
    align-items: center;

    img {
      width: 140px;
      height: 140px;
      object-fit: contain;
    }
  }
}

@media only screen and (max-width: 425px) {
    .cart-image{
        display:flex;
        flex-direction: column;
    }
}
</style>
