<template>
  <div>
    <h1>hi</h1>
    <input type="text" v-model="inputValue" />
    <input type="text" v-model="inputCount" />
    <input type="text" v-model="inputName" />
    <hr />
    <h4>{{inputName}} 님의 {{ inputValue }} 값은 {{inputCount}} 개 입니다.</h4>
    <hr />
      <div v-for="(cardObj,order) in titles" :key="order">
        {{ cardObj }}
        <card-ui
          :menuTitle="order + ' 번째 반복 - ' + cardObj.title"
          :menuCount="cardObj.menuCount"
          :backbroundColor="cardObj.bgColor"
          />
      </div>
  </div>
</template>

<script>
// define -> 정의
import CardUi from './ui-items/card-ui.vue'
export default {
  data(){
    return {
      inputValue : 'default value',
      inputCount : 'default count',
      inputName : 'default name',
      titles : [
        {
          title : '동해물과 백두산이',
          menuCount : 10,
          bgColor : 'red',
        },
        {
          title : '마르고 닳도록',
          menuCount : 2,
          bgColor : 'blue',
        },
        {
          title : '동해물과 백두산이',
          menuCount : 3,
          bgColor : 'black',
        },
        {
          title : '동해물과 백두산이',
          menuCount : 2,
          bgColor : 'green',
        },
        {
          title : '동해물과 백두산이',
          menuCount : 1,
          bgColor : 'yellow',
        },
      ],
    }
  },
  //등록
  components : {
    CardUi,
  }
}
</script>

<style>
body{
  background:#eee;
}
</style>