<template>
  <div class="gallery">
    <div
      v-for="(photo, idx) in photos"
      :key="idx"
      class="gallery-photo"
    >
      <img
        v-img="{ group: '1' }"
        :src="photo.url"
        class="gallery-img"
      >
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      photos: [
        {
          url: require('~/assets/images/2020-06-11_Frame-16.JPG')
        },
        {
          url: require('~/assets/images/2020-06-11_Frame-34.JPG')
        },
        {
          url: require('~/assets/images/DSC07712.jpg')
        },
        {
          url: require('~/assets/images/IMG_0172-2.jpg')
        },
        {
          url: require('~/assets/images/IMG_8317-2.jpg')
        },
        {
          url: require('~/assets/images/IMG_8798.jpg')
        },
        {
          url: require('~/assets/images/IMG_8915-м.jpg')
        },
        {
          url: require('~/assets/images/IMG_9939.jpg')
        },
        {
          url: require('~/assets/images/IMG_8798.jpg')
        },
        {
          url: require('~/assets/images/IMG_8915-м.jpg')
        },
        {
          url: require('~/assets/images/IMG_9939.jpg')
        }
      ]
    }
  }
}
</script>

<style scoped>
.gallery {
  /* Prevent vertical gaps */
   line-height: 0;
   -webkit-column-count: 5;
   -webkit-column-gap:   0px;
   -moz-column-count:    5;
   -moz-column-gap:      0px;
   column-count:         5;
   column-gap:           0px;
}

.gallery-photo:hover {
  opacity: .75;
  transition: opacity .5s ease;
}

.gallery-img {
  /* Just in case there are inline attributes */
  width: 100%;
  cursor: pointer;
}

@media (max-width: 1200px) {
  .gallery {
    -moz-column-count:    4;
    -webkit-column-count: 4;
    column-count:         4;
  }
}
@media (max-width: 1000px) {
  .gallery {
    -moz-column-count:    3;
    -webkit-column-count: 3;
    column-count:         3;
  }
}
@media (max-width: 800px) {
  .gallery {
    -moz-column-count:    2;
    -webkit-column-count: 2;
    column-count:         2;
  }
}
@media (max-width: 400px) {
  .gallery {
    -moz-column-count:    1;
    -webkit-column-count: 1;
    column-count:         1;
  }
}
</style>
