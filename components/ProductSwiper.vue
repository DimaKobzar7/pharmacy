<template>
  <swiper
    :slides-per-view="1"
    :space-between="100"
    :navigation="{
      prevEl: prev,
      nextEl: next,
    }"
    :modules="modules"
  >
    <swiper-slide>
      <img src="../assets/img/slide1.png" alt="slide1" />
    </swiper-slide>
    <swiper-slide>
      <img src="../assets/img/slide2.png" alt="slide2" />
    </swiper-slide>
    <swiper-slide>
      <img src="../assets/img/slide3.png" alt="slide3" />
    </swiper-slide>
    <swiper-slide>
      <img src="../assets/img/slide4.png" alt="slide4" />
    </swiper-slide>
    <swiper-slide>
      <img src="../assets/img/slide5.png" alt="slide5" />
    </swiper-slide>
    <div ref="prev" class="swiper-button-prev">
      <svg class="d-xxl-none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
        <path d="M14 17a1 1 0 0 1-.707-.293l-4-4a1 1 0 0 1 0-1.414l4-4a1 1 0 1 1 1.414 1.414L11.414 12l3.293 3.293A1 1 0 0 1 14 17z" />
      </svg>
      <svg class="d-none d-xxl-block" width="22" height="16" viewBox="0 0 22 16" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path
          d="M7.18546 0.240635C7.48517 -0.0802098 7.98399 -0.0802097 8.29419 0.240635C8.5939 0.550629 8.5939 1.06657 8.29419 1.37585L2.67228 7.19069L21.2238 7.19069C21.6563 7.19142 22 7.54691 22 7.99425C22 8.44149 21.6563 8.80857 21.2238 8.80857L2.67228 8.80856L8.29419 14.6126C8.5939 14.9335 8.5939 15.4501 8.29419 15.7594C7.98399 16.0802 7.48447 16.0802 7.18546 15.7594L0.232644 8.56798C-0.0775499 8.258 -0.0775499 7.74198 0.232644 7.43272L7.18546 0.240635Z"
        />
      </svg>
    </div>
    <div ref="next" class="swiper-button-next">
      <svg class="d-xxl-none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
        <path d="m14.707 12.707-4 4a1 1 0 0 1-1.414-1.414L12.586 12 9.293 8.707a1 1 0 1 1 1.414-1.414l4 4a1 1 0 0 1 0 1.414z" />
      </svg>
      <svg class="d-none d-xxl-block" width="22" height="16" viewBox="0 0 22 16" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path
          d="M14.8145 15.7594C14.5148 16.0802 14.016 16.0802 13.7058 15.7594C13.4061 15.4494 13.4061 14.9334 13.7058 14.6242L19.3277 8.80931L0.7762 8.80931C0.343699 8.80859 6.59772e-07 8.45309 6.98879e-07 8.00575C7.37978e-07 7.55851 0.343699 7.19143 0.7762 7.19143L19.3277 7.19144L13.7058 1.38738C13.4061 1.06653 13.4061 0.549893 13.7058 0.240633C14.016 -0.0802104 14.5155 -0.0802104 14.8145 0.240633L21.7674 7.43202C22.0775 7.742 22.0775 8.25802 21.7674 8.56728L14.8145 15.7594Z"
        />
      </svg>
    </div>
  </swiper>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation } from 'swiper';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },

  setup() {
    const prev = ref(null);
    const next = ref(null);

    return {
      modules: [Navigation],
      prev,
      next,
    };
  },
};
</script>
