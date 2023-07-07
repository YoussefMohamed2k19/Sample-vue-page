<template>
  <div class="container">
    <!-- Category Buttons -->
    <div>
      <h1 class="font-bold display-4 mt-4 mb-4">Our <br />Projects</h1>
      <a
        v-for="category in categories"
        :key="category"
        @click="selectCategory(category)"
        :class="{
          'active-btn': selectedCategory === category,
          'nonActive-btn': selectedCategory !== category,
        }"
        class="btn btn-sm mx-1 my-4 category-headline"
      >
        {{ category }}
      </a>
    </div>

    <!-- Image Gallery -->
    <div class="row mt-4">
      <div
        class="col-md-6 mb-4"
        v-for="image in filteredImages"
        :key="image.id"
      >
        <img
          :src="`${image.src}`"
          :alt="image.alt"
          class="img-fluid"
          style="border-radius: 25px"
        />

        <div>
          <h4 class="image-title font-bold">{{ image.title }}</h4>
          <div class="project-links-wrap">
            <div class="project-link-icon"></div>
            <div class="project-link-text">View Study Case</div>
            <div class="project-link-icon eye"></div>
            <div class="project-link-text">Live Preview</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ImageGallery",
  data() {
    return {
      categories: ["Web Design", "Mobile App Design", "Freebies"],
      selectedCategory: "Web Design",
      images: [
        {
          id: 1,
          src: "./assets/image1.png",
          alt: "Image 1",
          category: "Mobile App Design",
          title: "Minify - Web Design",
        },
        {
          id: 2,
          src: "../assets/image2.png",
          alt: "Image 2",
          category: "Mobile App Design",
          title: "Ant - Personal Portofolio",
        },
        {
          id: 3,
          src: "../assets/image3.jpg",
          alt: "Image 3",
          category: "Freebies",
          title: "Lumy - Dashboard UI Kit",
        },
        {
          id: 4,
          src: "../assets/image4.jpeg",
          alt: "Image 4",
          category: "Freebies",
          title: "Keeper - Soccer Site",
        },
        // Add more images with respective categories
      ],
    };
  },
  computed: {
    filteredImages() {
      if (this.selectedCategory === "Web Design") {
        return this.images;
      } else {
        return this.images.filter(
          (image) => image.category === this.selectedCategory
        );
      }
    },
  },
  methods: {
    selectCategory(category) {
      this.selectedCategory = category;
    },
  },
};
</script>

<style>
.category-headline {
  font-size: 32px;
  font-weight: bold;
  padding-right: 30px;
}
.active-btn {
  color: #eebf63;
  text-underline-offset: 25px;
  text-decoration: underline #eebf63 5px;
}
.nonActive-btn {
  color: grey;
}
.image-title {
  margin-top: 30px;
  margin-bottom: 16px;
}
.project-links-wrap {
  display: flex;
  align-items: center;
}
.project-link-text {
  padding-right: 40px;
}
.project-link-icon {
  width: 18px;
  height: 18px;
  margin-right: 13px;
  background-image: url("../icons/layers-icon.svg");
  background-position: 50% 50%;
  background-size: contain;
  background-repeat: no-repeat;
}
.project-link-text {
  color: #151517;
}
.project-link-icon.eye {
  background-image: url("../icons/eye-icon.svg");
}
</style>
