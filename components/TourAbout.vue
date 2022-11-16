<script>
export default {
  name: 'TourAbout',
}
</script>
<template>
  <div class="about-hero container">
    <div class="about-title">
      <p>
        <span> {{ $t('why') }} </span>

        {{ $t('aboutText') }}
      </p>
      <br />
      <p>
        <span>
          {{ $t('meals') }}
        </span>
        {{ $t('dinnerText') }}
      </p>
      <br />

      <p>{{ $t('familyVisa') }}</p>
    </div>
    <div class="about-image">
      <img src="../assets/images/about-image.png" alt="" />
    </div>
  </div>
</template>
<style>
.about-hero {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 48px;
}
.about-title {
  width: 500px;
  height: auto;
}
span {
  color: #a87d32;
}

@media only screen and (max-width: 425px) {
.about-hero{
    display:flex;
    flex-direction: column;
}

.about-title{
    width:100%;
    padding:12px;
}
}
</style>
