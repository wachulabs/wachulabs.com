<template>
  <section class="hero-section" id="hero">
    <div class="wave">
      <svg
        width="100%"
        height="355px"
        viewBox="0 0 1920 355"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
      >
        <g
          id="Page-1"
          stroke="none"
          stroke-width="1"
          fill="none"
          fill-rule="evenodd"
        >
          <g
            id="Apple-TV"
            transform="translate(0.000000, -402.000000)"
            fill="#FFFFFF"
          >
            <path
              d="M0,439.134243 C175.04074,464.89273 327.944386,477.771974 458.710937,477.771974 C654.860765,477.771974 870.645295,442.632362 1205.9828,410.192501 C1429.54114,388.565926 1667.54687,411.092417 1920,477.771974 L1920,757 L1017.15166,757 L0,757 L0,439.134243 Z"
              id="Path"
            ></path>
          </g>
        </g>
      </svg>
    </div>

    <div class="container">
      <div class="row align-items-center">
        <div class="col-12 hero-text-image">
          <div class="row">
            <div
              class="col-lg-8 text-center text-lg-start animate__animated animate__fadeInLeft"
            >
              <h1 data-aos="fade-right">Promote Your API with Beast API</h1>

              <p
                class="mb-5"
                data-aos="fade-right"
                data-aos-delay="100"
                :class="{ 'aos-init aos-animate': view.slowShow }"
              >
                Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              </p>
              <p
                data-aos="fade-right"
                data-aos-delay="200"
                data-aos-offset="-500"
                :class="{ 'aos-init aos-animate': view.slowShow }"
              >
                <router-link to="#" class="btn btn-outline-white"
                  >Get started</router-link
                >
              </p>
            </div>
            <div
              class="col-lg-4 iphone-wrap animate__animated animate__fadeInRight"
            >
              <img
                :src="view.img1"
                alt="Image"
                class="phone-1"
                data-aos="fade-right"
              />
              <img
                :src="view.img2"
                alt="Image"
                class="phone-2"
                data-aos="fade-right"
                data-aos-delay="200"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import img1 from "@/assets/img/phone_1.png";
import img2 from "@/assets/img/phone_2.png";
export default {
  data() {
    return {
      view: {
        slowShow: false,
        img1: img1,
        img2: img2,
      },
    };
  },
  mounted() {
    this.handleAnimation();
  },
  methods: {
    handleAnimation() {
      setTimeout(() => {
        this.view.slowShow = true;
      }, 1000);
    },
  },
};
</script>
<style scoped>
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}
@media screen and (max-width: 992px) {
  .hero-section {
    height: 154vh;
  }
  .hero-section .iphone-wrap .phone-1 {
    margin-left: 20%;
  }
  .hero-section .iphone-wrap .phone-2 {
    margin-left: 20%;
  }
}

@media screen and (max-width: 576px) {
  .hero-section .iphone-wrap .phone-2 {
    margin-left: 7%;
  }
}

</style>



