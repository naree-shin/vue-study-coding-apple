<template>
  <div>

    <!-- 모달팝업 -->
    <div class="black-bg" v-if="모달창 == true">
      <div class="white-bg">
        <h4>상세페이지</h4>
        <p>상세페이지 내용</p>
        <button @click="모달창 = false">닫기</button>
      </div>
    </div>

    <!-- 메뉴 -->
    <div class="menu">
      <a v-for="a in menuArray" :key="a">{{a}}</a>
    </div>

    <div>
      <!-- 속성안에 데이터바인딩 속성앞에 : 를 붙여야함 -->
      <img :src="원룸들[0].image" class="room-img">
      <h4>{{원룸들[0].title}} 원룸</h4>
      <p>{{원룸들[0].price}}원</p>
    </div>

  </div>
</template>

<script>
// oneroom.js -> export default apple
import data01 from './assets/js/data/oneroom.js';

export default {
  name: 'App',
  data(){
    return {
      원룸들 : data01,
      모달창 : false,
      신고수 : [0,0,0],
      menuArray : ['Home','Shop','About'],
      shop : ['역삼동','천호동','마포구']
      
    }
  },
  methods : {
    increase() {
      this.신고수 += 1;
    }
  },
  components: {
  }
}
</script>

<style>
/* 모달팝업 */
body {
  margin: 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}
.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
.room-img {
  width: 100%;
  margin-top: 40px;
}



</style>
