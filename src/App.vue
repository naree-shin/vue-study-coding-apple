<template>
  <div>
    <!-- 메뉴 -->
    <div class="menu">
      <a v-for="a in menuArray" :key="a">{{a}}</a>
    </div>

    <div>
      <h4>{{shop[0]}} 원룸</h4>
      <p>50 만원</p>

      <!-- 기존 javascript -->
      <!-- <button onclick="">허위매물신고</button> <span>신고수 : 0</span> -->
      
      <!-- vue 문법 -->
      <!-- <button v-on:click="자바스크립트">허위매물신고</button> <span>신고수 : 0</span> -->
      <!-- 'v-on:' -> '@' 로 축약가능  -->
      <!-- '변수++' -> 변수에 1 더하기  -->
      <!-- <button @click="신고수++">허위매물신고</button> <span>신고수 : {{신고수}}</span> -->
      <button @click="increase">허위매물신고</button> <span>신고수 : {{신고수}}</span>
    </div>
    <div>
      <h4>{{shop[1]}} 원룸</h4>
      <p>50 만원</p>
    </div>
    <div>
      <h4>{{shop[2]}} 원룸</h4>
      <p>50 만원</p>
    </div>

  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      신고수 : 0,
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
</style>
