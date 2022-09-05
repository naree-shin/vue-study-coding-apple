<template>
  <!-- 모달팝업 -->
    <div class="black-bg" v-if="모달창 == true">
      <div class="white-bg">
        <img :src="원룸들[누른거].image" style="width:100%">
        <h4>{{원룸들[누른거].title}}</h4>
        <p>{{원룸들[누른거].content}}</p>
        <p>{{원룸들[누른거].price}} 원</p>
        <button @click="모달창 = false">닫기</button>
      </div>
    </div>
</template>

<script>
export default {
  name: 'ModalPop',
}
</script>

<style>

</style>