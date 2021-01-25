<template>
<form @submit="formSubmit" @reset="formReset" >
  <view>
    <view class="formulaTitle">参数一：</view>
    <input class="formulaCt input" v-model="data1" type="number" />
    <view class="formulaTitle">参数一：</view>
    <input class="formulaCt input" v-model="data2" type="number"/>
    <button @tap="addNumber">Add new number</button>
  </view>
</form>
</template>

<script>
export default {
  name: 'NumberSubmit',
  data() {
    return {
      data1:'',
      data2:''
    }
  },
  methods: {
    addNumber() {
      this.$store.dispatch('addNumber', this.data1)
    },
    formSubmit(){

    },
    formReset(){

    }
  }
}
</script>

<style>
.formulaTitle{

}
.formulaCt.input{
  border-bottom: 1px solid #ddd;
  margin: 10px;
}
</style>

