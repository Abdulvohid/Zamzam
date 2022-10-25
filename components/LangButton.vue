<script>
export default {
  name: 'LanguageButton',
  components: {
  },
  props: {
    langOptins: {
      type: Array,
      default: () => [],
    },
  },
  data() {
    return {
      loacale: this.$i18n.locale,
      list: {
        'ru': 'Ru',
        'en': 'En',
        'uz': 'Uz'
      }
    }
  },
  watch: {
    '$i18n.locale' (event) {
      this.$router.push(this.switchLocalePath(event))
    },
  },
}
</script>

<template>
  <!-- selectga icon qo'yib ketish kerak. Qo'yib qo'yilsin -->

  <div>
   
    <select             v-model="$i18n.locale"
 >
 <option v-for="(item, index) in $i18n.locales"  :key="index" :value="item">
            {{list[item]}}
          </option>
    </select>
  </div>
</template>

<style lang="scss" scoped></style>