<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!--안녕하세요. -->
<div>
  <h4 class="red" style="스타일">{{ products[0]}}</h4>
  <p>{{ price1 }} 만원</p>
</div>
<div>
  <h4>{{ products[1] }}</h4>
  <p>{{ price2 }} 만원</p>
</div>
<div>
  <h4>{{ products[2]}}</h4>
  <p>{{ price3 }} 만원</p>
</div>
</template>

<script>
// document.getElementById().innerHTML = ??  //원래 쌩 자바스크립트 형식 입력, vue에선 아래 추가하면서 간단히 만들어서 데이터 보관 할 수 있다. 


export default {
  name: 'App',
  data() {
    return {
      price1 : 50,      //위와 맞춰준다! , 자료이름: 자료내용
      price2 : 60,
      price3 : 40,
      // 또는 prices: [50,60,40] 형식으로 한번에 배열로 저장하고, 위도 idex맞춰줄 수 있다!

      products : ['역삼동원룸', '천호동원룸', '마포구원룸']
    }
  },
  components: {
  
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
