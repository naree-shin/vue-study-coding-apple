<template>
  <div>
    <!-- 메뉴 -->
    <div class="menu">
      <a v-for="a in menuArray" :key="a">{{a}}</a>
    </div>

    <div>
      <!-- 신고수버튼 여러개 만들기-->
      
      <img src="./assets/images/room0.jpg" class="room-img">
      <h4>{{shop[0]}} 원룸</h4>
      <p>50 만원</p>
      <button @click="신고수[0] += 1">허위매물신고</button>
      <span>신고수 : {{신고수[0]}}</span>
    </div>
    <div>
      <img src="./assets/images/room1.jpg" class="room-img">
      <h4>{{shop[1]}} 원룸</h4>
      <p>50 만원</p>
      <button @click="신고수[1] += 1">허위매물신고</button>
      <span>신고수 : {{신고수[1]}}</span>
    </div>
    <div>
      <img src="./assets/images/room2.jpg" class="room-img">
      <h4>{{shop[2]}} 원룸</h4>
      <p>50 만원</p>
      <button @click="신고수[2] += 1">허위매물신고</button>
      <span>신고수 : {{신고수[2]}}</span>
    </div>


  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
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
