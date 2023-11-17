<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'

let isSignin: boolean = false;


</script>

<template>
  <div v-if="isSignin" class="wrapper">
    <header>
      <div class="headerWrapper">


        <nav>
          <RouterLink to="/">메인</RouterLink> |
          <RouterLink to="/about">채팅</RouterLink>
        </nav>

        <!-- <div>메뉴 부분은 라우터 링크로 채운다</div>
      <div>라우터 뷰는 채팅 내용으로 채운다</div>
      <div>메뉴 부분에 내 정보와 채팅 헤드를 넣는다</div>
      <div>라우터뷰 부분에 채팅 내용으로 채운다</div>

      <div>모바일 우선으로 만들어야 한다</div>
      <div>모바일 뷰 우선으로 상단에 메뉴를 넣고 상단에 내용 넣기</div> -->
      </div>
    </header>
    <RouterView />
  </div>
  <div v-else>
    <span>인증해주세요</span>

    <div>
      <input type="email" placeholder="이메일">
    </div>
    <div>
      <input type="password" placeholder="비밀번호">
    </div>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
}

nav {
  width: 100%;
  height: 50px;
  background-color: aquamarine;
}
</style>
