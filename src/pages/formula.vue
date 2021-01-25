<template>
<form @submit="formSubmit" @reset="formReset" >
  <view class="formula">
    <view class="formulaTitle">参数一：</view>
    <input class="formulaCt input" v-model="data1" type="number" />
    <view class="formulaTitle">参数一：</view>
    <input class="formulaCt input" v-model="data2" type="number"/>
    <view class="formulaResult">公式计算结果：{{sum}}</view>
    <button @tap="addNumber">保存</button>
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
  computed:{
    sum(){
      return this.data1*1+this.data2*1;
    }
  },

  methods: {
    addNumber() {
      this.$store.dispatch('addNumber', this.sum)
    },
    formSubmit(){

    },
    formReset(){

    }
  }
}
</script>

<style lang="less">
.formula{
  padding:16Px;
  .formulaTitle{margin-top:10Px;}
  .formulaCt.input{border-bottom: 1Px solid #ddd;line-height:30Px;}
  .formulaResult{margin:10Px 0;line-height:30Px;}
}

</style>

