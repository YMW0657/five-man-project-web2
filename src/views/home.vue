
<template>
  <div class="index">
    <div class="home-wrapper">
      <div class="header">
        <div class="logo">
          <img src="@/assets/img/img01.png" alt="">
        </div>
      </div>
      <div class="content">
        <div class="main-page">
          <img src="@/assets/img/img02.png" alt="">
        </div>
        <div class="btn-group">
          <a-button type="primary" @click="toDashboardFn">Start Now</a-button>
        </div>
      </div>
    </div>
  </div>

</template>
<script setup>
  import { useRouter } from "vue-router";
  const router = useRouter();
  const toDashboardFn = ()=>{
    router.push("/dashboard");
  }
</script>
<style scoped>
  .index{
    width:100%;
    height: 100%;
    position: relative;
  }
  .home-wrapper {
    font-size: 20px;
    line-height: 36px;
  }
  .home-wrapper .header{
    width: 100%;
    height: 110px;
    background-color: #135592;
    padding:0 30px;
  }
  .home-wrapper .header .logo{
    height: 100%;
    display: flex;
    align-items: center;
  }
  .home-wrapper .header .logo img{
    width: 64px;
  }
  .home-wrapper .content{
    height: calc(100vh - 110px);
    background-color: #89aac8;
    overflow: hidden;
  }
  .content .main-page img {
    width: 80%;
    display: block;
    margin:30px auto;
  }
  .home-wrapper .content .btn-group{
    display: flex;
    justify-content: center;
  }
  .home-wrapper .content .btn-group button{
    background-color: #135592;
    letter-spacing: 1px;
    font-weight: bold;
  }
  .home-wrapper .content .btn-group button:hover{
    background-color: #1569b8;
  }
</style>
