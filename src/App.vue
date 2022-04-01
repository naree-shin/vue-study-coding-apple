<template>
  <div>
    <div>
      <h4>XX 원룸</h4>
      <!-- 자료 불러올때 {{ 자료이름 }}-->
      <p>{{price1}} 만원</p>
    </div>
    <div>
      <h4>XX 원룸</h4>
      <p :style="style01">{{ price2 }} 만원</p>
    </div>
    <div>
      <!-- array -->
      <h4>{{shop[0]}} 원룸</h4>
      <p>{{ price2 }} 만원</p>
    </div>
    <div>
      <h4>{{shop[1]}} 원룸</h4>
      <p>{{ price2 }} 만원</p>
    </div>
    <div>
      <h4>{{shop[2]}} 원룸</h4>
      <p>{{ price2 }} 만원</p>
    </div>

    <!-- html반복문 -->
    <div class="menu">
      <a v-for="작명 in 반복횟수" :key="작명">Home</a>
      <!-- 작명은 a 나 i로 쓰는경우가 많음 -->

      <a v-for="menuItem in 3" :key="menuItem">menu</a>
      <br>
      <br>
      <!-- 데이터 넣는것도 가능 -->
      <a v-for="작명 in 데이터" :key="작명">작명</a>
      <a v-for="a in menuArray" :key="a">{{a}}</a>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      // 데이터영역
      // 데이터는 object 자료형식으로 저장
      // {자료이름:자료내용}
      price1 : 60,
      price2 : 70,
      // html 속성도 데이터 바인딩 가능
      style01 : 'color : blue', 
      // array
      menuArray : ['Home','Shop','About'],
      shop : ['역삼동원룸','천호동원룸','마포구원룸']


    }
  },
  components: {
  }
}
</script>

<style>
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>
