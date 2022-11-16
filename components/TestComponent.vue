<script>
export default {
  name: 'test-component',

  data() {
    return {
      toggle: true,
    }
  },

  methods: {
    toggleButton() {
      this.toggle = !this.toggle
      console.log('ishladi')
    },
  },
}
</script>
<template>
  <div class="test-hero" v-if="toggle">
    <div class="test-title" v-if="toggle">
      {{ $t('testText') }}
    </div>

    <button class="test-btn" v-if="toggle" @click="toggleButton()">
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
  </div>
</template>

<style lang="scss">
.test-hero {
  width: 100%;
  height: 40px;
  background: #11795f;
  color: #fff;
  display: flex;
  align-items: center;
  padding: 8px;
}

.test-title {
  text-align: center;
  margin: 0 auto;
}

.test-btn {
  background: none;
  border:none;
  border-color: #fff;
  width: 40px;
  height: 40px;
}
</style>
