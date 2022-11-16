<script>
export default {
  name: 'TourInfo',
  data() {
    return {}
  },
}
</script>

<template>
  <div class="tour-hero">
    <h2>{{$t('package')}}</h2>
    <div class="tour-info">
      <div class="tour-list">
        <div class="tour-list_item">
          <ul>
            <h2>{{$t('visit')}}</h2>
            <b>{{$t('mecca')}} :</b>
            <li>{{$t('savr')}}</li>
            <li>{{$t('nur')}}</li>
            <li>{{$t('arafat')}}</li>
            <li>{{$t('muzdalifa')}},</li>
            <li>{{$t('mino')}},</li>
            <li>{{$t('jamorot')}},</li>
            <li>{{$t('mosque')}},</li>
            <li>{{$t('muallo')}}.</li>
          </ul>
        </div>
      </div>
      <div class="tour-list">
        <div class="tour-list_item">
          <ul>
            <h2>{{$t('visit')}}</h2>
            <b>{{$t('madina')}} :</b>
            <li>{{$t('qubo')}}</li>
            <li>{{$t('qibla')}}</li>
            <li>{{$t('Xandaq')}}</li>
            <li>{{$t('quran')}}</li>
            <li>{{$t('uhud')}},</li>
            <b>{{$t('amenit')}}:</b>

            <li>{{$t('dinner')}};</li>
            <li>{{$t('transfer')}};</li>
            <li>{{$t('travel')}}</li>
            <li>{{$t('git')}};</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.tour-hero {
  margin-top: 120px;
  h2 {
    color: #11795f;
    text-align: center;
    font-size: 52px;
  }

  .tour-info {
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  .tour-list {
    background-color: #11795f;
    width: 280px;
    height: 488px;
    margin-top: 32px;
  }

  .tour-list_item {
    ul {
      padding: 20px;
      h2 {
        color: #fff;
        font-size: 24px;
        font-weight: 400;
        margin-bottom: 12px;
      }
      b {
        font-weight: 400;
        color: gold;
        font-style: italic;
        margin: 10px 0 !important;
      }

      li {
        color: #fff;
        font-size:20px;
        text-align:center;
        list-style: none;
      }
    }
  }
}

@media only screen and (max-width: 425px) {
    .tour-hero {
  h2 {
    
    font-size: 32px;
  }}

  .tour-info{
    display: flex;
    flex-direction:column;
    .tour-list{
    width: 100%;
    height: 100%;
  }
  }



}
</style>
