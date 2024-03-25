<template>
  <div class="py-5 mt-3 mt-lg-5">
    <section>
      <div class="container-xl">
        <div class="row">
          <div class="col-lg-5 d-flex align-items-center justify-content-center">
            <img class="aboutImg w-100" src="../assets/about.png" alt="">
          </div>
          <div class="col-lg-7 ps-lg-5">
            <h2 class="about-text page-title mt-5 mt-lg-0">About Us</h2>
            <p class="mt-4 mb-4">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed tempus orci sed leo fermentum, sit amet
              lobortis nisi congue.
            </p>
            <article>
              <ul class="list-group">
                <li class="list-group-item"><i class="bi bi-check-lg"></i> An item</li>
                <li class="list-group-item"><i class="bi bi-check-lg"></i> A second item</li>
                <li class="list-group-item"><i class="bi bi-check-lg"></i> A third item</li>
                <li class="list-group-item"><i class="bi bi-check-lg"></i> A fourth item</li>
                <li class="list-group-item"><i class="bi bi-check-lg"></i> And a fifth one</li>
              </ul>
            </article>

            <p class="mt-4 text-body-tertiary fs-7">
              Lorem ipsum dolor sit amet,<br> consectetur adipiscing elit.<br> Aenean et nequeeger a commodo velit,<br> a bibendum quam. <br>Integer faucibus purus id congue preti
            </p>

          </div>
        </div>
      </div>
    </section>
  </div>
  <Footer></Footer>
</template>

<script setup>
import Footer from '@/components/Footer.vue';
</script>

<style lang="scss" scoped>
.aboutImg {
  @media (max-width:992px){
    width:75% !important;
  }
}

</style>