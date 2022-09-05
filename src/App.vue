<template>
  <div>

    <modal-pop></modal-pop>

    <!-- 메뉴 -->
    <div class="menu">
      <a v-for="a in menuArray" :key="a">{{a}}</a>
    </div>

    <discount-banner></discount-banner>

    <div v-for="(a, i) in 원룸들" :key="i">
      <!-- 속성안에 데이터바인딩 속성앞에 : 를 붙여야함 -->
      <img :src="a.image" class="room-img">
      <h4 @click="모달창 == true; 누른거 = i">{{a.title}} 원룸</h4>
      <p>{{a.price}}원</p>
    </div>

  </div>
</template>

<script>
// oneroom.js -> export default apple
import data01 from './assets/js/data/oneroom.js';
import DiscountBanner from './components/DisconutBanner';
import ModalPop from './components/ModalPop';

export default {
  name: 'App',
  data(){
    return {
      원룸들 : data01,
      누른거: 0,
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
    DiscountBanner,
    ModalPop,
  }
}
</script>

<style>
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
