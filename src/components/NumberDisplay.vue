<template>
  <view>
    <text class="title">{{ getNumbers.join(',') }}</text>
  </view>
</template>

<script>
export default {
  name: 'NumberDisplay',
  computed: {
    getNumbers() {
      return this.$store.getters.getNumbers;
    }
  }
}
</script>

<style>
.title {
  font-size: 40px;
}
</style>
