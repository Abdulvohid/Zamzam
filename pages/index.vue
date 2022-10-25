<template>
  <div>



<LangButton/>

<h2>{{ $t('hello') }}</h2>
</div>

</template>

<script>
export default {
  name: 'IndexPage',
  components: 'LangButton'
}
</script>
