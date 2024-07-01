<template>

  <div class="menu">
    <!-- <a>Home</a> -->
    <!-- <a>Products</a>      <a>태그 여러개 이런식으로 일일히 입력할 수도 있지만, 반복문일때 간단히 한번에 쓰는 방법 밑에!!
    <a>About</a> -->
    <a v-for="a in 메뉴들" :key="a">{{ a }}</a>           <!-- 또는 2개까지 넣는거 가능해서 <a v-for="(a,i) in 메뉴들" :key="a">{{ i }}</a> -->
  </div>

  <div>
    <h4>{{ products[0] }}</h4>
  <p>50 만원</p>
  <!-- <button @:click="신고수 += 1">허위매물신고</button> <span>신고수 : {{ 신고수 }}</span> -->
  <!-- <button @:mouseover="신고수 += 1">허위매물신고</button> <span>신고수 : {{ 신고수 }}</span> -->
  <button @:click="increase">허위매물신고</button> <span>신고수 : {{ 신고수 }}</span>
</div>
<div>
  <h4>{{ products[1]}}</h4>
  <p>60 만원</p>
</div>
<div>
  <h4>{{ products[2]}}</h4>
  <p>40만원</p>
</div>

</template>

<script>
// document.getElementById().innerHTML = ??  //원래 쌩 자바스크립트 형식 입력, vue에선 아래 추가하면서 간단히 만들어서 데이터 보관 할 수 있다. 


export default {
  name: 'App',
  data() {
    return {
      신고수 : 0,
      메뉴들 : ['Home', 'Shop', 'About'],
      // price1 : 50,      //위와 맞춰준다! , 자료이름: 자료내용
      // price2 : 60,
      // price3 : 40,
      // 또는 간단히!! prices: [50,60,40],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸']
    }
  },

  methods: {
    increase(){
     this.신고수 +=1
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
}

.menu {
  background : darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}

</style>
