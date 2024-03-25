<template>
  <div class="py-5 mt-3 mt-lg-5">
    <section>
      <div class="container-xl">
        <div class="portfolio-text text-center">
          <h2 class="d-inline-block page-title mt-5 mt-lg-0">portfolio</h2>
          <p class="d-none d-md-block  mb-5 mt-5">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed tempus orci sed leo fermentum, sit amet
            lobortis nisi congue.
          </p>
        </div>
        <section class="portfolio-tab mb-5">
          <div class="text-center">
            <button class="btn mx-2" @click="activePf = 'mobileApp'"
              :class="activePf === 'mobileApp' ? 'btn-danger' : 'btn-outline-secondary'">
              Mobile App
            </button>
            <button class="btn mx-2" @click="activePf = 'resWeb'"
              :class="activePf === 'resWeb' ? 'btn-danger' : 'btn-outline-secondary'">
              Responsive Web
            </button>
            <button class="btn mx-2" @click="activePf = 'frontWeb'"
              :class="activePf === 'frontWeb' ? 'btn-danger' : 'btn-outline-secondary'">
              Frontend Web
            </button>
          </div>
        </section>
        <div class="">
          <div class="row row-gap-4">
            <slot v-if="activePf === 'mobileApp'">
              <div class="col-sm-6 col-lg-4 col-xl-3" v-for="(item, Idx) in mobileApps" :key="Idx"
                data-bs-toggle="modal" :data-bs-target="`#item${idx}`">
                <div class="card" style="cursor:pointer;">
                  <div class="card-img-wrap">
                    <img :src="item.image" class="card-img-top h-100 object-fit-cover" alt="image">
                  </div>
                  <div class="card-img-overlay"></div>
                  <div class="card-body">
                    <h5 class="card-title">{{ item.title }}</h5>
                    <p class="card-text">Some quick example text to build on the card.</p>
                  </div>
                </div>
                <div class="modal" :id="`item${idx}`" tabindex="-1" aria-labelledby="exampleModalLabel"
                  aria-hidden="true">
                  <div class="modal-dialog">
                    <div class="modal-content">
                      <div class="modal-header">
                        <h1 class="modal-title fs-5" id="exampleModalLabel">{{ item.title }}</h1>
                        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                      </div>
                      <div class="modal-body">
                        <img :src="item.image" alt="">
                      </div>
                      <div class="modal-footer">
                        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </slot>
            <slot v-if="activePf === 'resWeb'">
              <div class="col-sm-6 col-lg-4 col-xl-3" v-for="(res, resIdx) in resWebs" :key="resIdx">
                <div class="card">
                  <div class="card-img-wrap">
                    <img :src="res.image" class="align-end card-img-top object-fit-cover " alt="image">
                  </div>
                  <div class="card-img-overlay"></div>
                  <div class="card-body">
                    <h5 class="card-title">{{ res.title }}</h5>
                    <p class="card-text">Some quick example text to build on the card.</p>
                  </div>
                </div>
              </div>
            </slot>
            <slot v-if="activePf === 'frontWeb'">
              <div class="col-sm-6 col-lg-4 col-xl-3" v-for="(fro, froIdx) in frontWebs" :key="froIdx">
                <div class="card">
                  <div class="card-img-wrap">
                    <img :src="fro.image" class="align-end card-img-top object-fit-cover " alt="image">
                  </div>
                  <div class="card-img-overlay"></div>
                  <div class="card-body">
                    <h5 class="card-title">{{ fro.title }}</h5>
                    <p class="card-text">Some quick example text to build on the card.</p>
                  </div>
                </div>
              </div>
            </slot>


          </div>
        </div>

      </div>
    </section>
  </div>
  <Footer></Footer>
</template>

<script setup>
import Footer from '@/components/Footer.vue';
import { ref } from 'vue';

const activePf = ref('mobileApp')

const mobileAppImg = 'https://d3h2k7ug3o5pb3.cloudfront.net/image/2020-11-27/fad74b50-30a6-11eb-ae9f-09e7aa62c338.jpg';
const mobileApps = [
  { title: 'Mobile App1', image: 'https://d3h2k7ug3o5pb3.cloudfront.net/image/2020-11-27/fad74b50-30a6-11eb-ae9f-09e7aa62c338.jpg' },
  { title: 'Mobile App2', image: 'https://assets.justinmind.com/wp-content/webp-express/webp-images/uploads/2019/08/mobile-banking-app-design-best-ui-patterns-1.png.webp' },
  { title: 'Mobile App3', image: 'https://buildwithangga.com/storage/assets/portfolio/E2G3GbucuRPG5RYRuVVclMBsZoe1XZTrDe1sLQgg.png' },
  { title: 'Mobile App4', image: mobileAppImg },
  { title: 'Mobile App5', image: mobileAppImg }
]

const resWebImg = 'https://img.freepik.com/free-vector/gradient-responsive-website-design-set_23-2149538364.jpg?w=996&t=st=1711078512~exp=1711079112~hmac=ea7c1e76ec9cbe044bc3094423c9ee012ed13e5a33bbaff51697aa83cf1e61ef';
const resWebs = [
  { title: 'Responsive Web1', image: 'https://img.freepik.com/free-vector/gradient-responsive-website-design-set_23-2149538364.jpg?w=996&t=st=1711078512~exp=1711079112~hmac=ea7c1e76ec9cbe044bc3094423c9ee012ed13e5a33bbaff51697aa83cf1e61ef' },
  { title: 'Responsive Web2', image: resWebImg },
  { title: 'Responsive Web3', image: resWebImg },
]
const frontWebImg = 'https://gracethemes.com/wp-content/uploads/2023/03/blog-img.png';
const frontWebs = [
  { title: 'Frontend Web1', image: frontWebImg },
  { title: 'Frontend Web2', image: frontWebImg },
]

</script>

<style lang="scss" scoped>
.portfolio-tab {
  .btn {
    @media (max-width:390px) {
      font-size: 12px;
    }
  }
}

.card-img-wrap {
  width: 100%;
  height: 300px;
  overflow: hidden;
}

.card-img-overlay {
  background: rgb(156, 175, 170);
  background: linear-gradient(0deg, rgba(156, 175, 170, 0)0%, rgba(156, 175, 170, 0)70%, rgba(156, 175, 170, 0.18)90%, rgba(156, 175, 170, 0.5)100%);
}

.modal {
      --bs-modal-width: 70%;
      text-align: center;
  img {
      max-width:100%
    }
}

  @media (max-width:576px) {
    .btn { font-size: 14px; line-height: 1;
    }
  }
</style>