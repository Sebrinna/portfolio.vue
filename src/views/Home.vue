<template>
  <div class="py-5 mt-5 mt-lg-5">
    <section>
      <div class="container-xl">
        <div class="row">
          <div class="col-lg-6">
            <h2 class="intro-text">
              Welcome to<br>
              <p class="text-danger">VUE-BOOTSTRAP</p>
              <strong>Agency</strong>
            </h2>
            <p class="mb-5">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin dignissim massa sapien, ut
              malesuada enim vulputate eu. Cras dapibus ligula eget laoreet auctor. Donec vel condimentum neque, aliquam
              malesuada mauris.</p>
              <div class="">
                <a @click="$router.push('about')" href="#" class="btn btn-danger px-4 me-2 rounded-4">About Us</a>
                <a @click="$router.replace('portfolio')" href="#" class="btn btn-success px-4 rounded-4">Portfolio</a>
          
                  <!-- 프로그래밍 방식
                  $router.push('about') - 히스토리 스택에 추가
                  $router.replace('portfolio') - 히스토리 
                  $router.go(-1) - 한단계 뒤 -->
                
              </div>
          </div>
          <div class="col-lg-6 d-flex justify-content-center align-items-center mt-5 mt-lg-0">
            <img class="homeImg w-100" src="../assets/gate.png" alt="">
          </div>
        </div>
      </div>
    </section>
  </div>
  <Footer></Footer>
</template>

<script setup>
import Footer from '../components/Footer.vue'
</script>

<style lang="scss" scoped>

.intro-text {
  font-weight: 300;
  line-height: 1;
  font-size: 3rem;
  font-family: 'Teko', sans-serif;

  p {
    font-size: 6rem;
    text-transform: uppercase;
    font-weight: 600;
    margin: 30px 0 0px;
  }

  strong {
    font-size: 5rem;
    text-transform: uppercase;
    font-weight: 600;
  }

  &::after {
    display: block;
    content: "";
    width: 100px;
    height: 8px;
    background: #000;
    margin-top: 20px;
  }
}

.homeImg {
  @media (max-width:992px){
    width:75% !important;
  }
}
</style>