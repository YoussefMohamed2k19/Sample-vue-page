<template>
  <div class="footer">
    <div class="row">
      <div class="col-md-4 mt-2">
        <div class="logo-text">Let's Connect</div>
      </div>
      <div class="col-md-4 mt-2">
        <div class="social-icons-wrapper justify-content-center">
          <a href="#" class="social-icon w-inline-block"></a
          ><a href="#" class="social-icon youtube w-inline-block"></a
          ><a href="#" class="social-icon dribble w-inline-block"></a>
        </div>
      </div>
      <div class="col-md-4 mt-2">
        <div
          class="footer-text justify-content-md-center justify-content-md-end justify-content-lg-end"
          @click="scrollToTop"
          v-show="showButton"
        >
          Back to top
          <img src="../icons/arrow.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      showButton: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.showButton = window.scrollY > 200;
    },
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });
    },
  },
};
</script>

<style>
.footer {
  height: 100px;
}
.logo-text {
  font-weight: 600;
  font-size: 26px;
}
.social-icons-wrapper {
  display: flex;
}
.social-icon {
  width: 32px;
  height: 32px;
  margin-right: 12px;
  margin-left: 12px;
  background-image: url("../icons/instagram-icon.svg");
  background-position: 50% 50%;
  background-size: contain;
  background-repeat: no-repeat;
}
.social-icon.youtube {
  background-image: url("../icons/youtube-icon.svg");
}
.social-icon.dribble {
  background-image: url("../icons/dribble-icon.svg");
}

.footer-text {
  cursor: pointer;
  display: flex;
  font-size: 24px;
}
.footer-text img {
  width: 28px;
  height: 28px;
  margin-left: 8px;
  margin-top: 4px;
}
</style>
