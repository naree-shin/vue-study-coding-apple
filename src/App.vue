<template>
  <div>
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

    <!-- 작명은 2개까지 가능 -->
      <!-- a 는 shop안에 있던 데이터가 된다 -->
    <div v-for="(a,i) in shop" :key="a">
      <!-- <h4>{{shop[반복되면서0,1,2되는변수]}}원룸</h4> -->
      <h4>{{shop[i]}}원룸</h4>
      <p>50만원</p>
    </div>
    <!-- <div>
      <h4>{{shop[1]}} 원룸</h4>
      <p>{{ price2 }} 만원</p>
    </div>
    <div>
      <h4>{{shop[2]}} 원룸</h4>
      <p>{{ price2 }} 만원</p>
    </div> -->

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
