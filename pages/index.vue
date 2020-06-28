<template>
  <div class="band">
    <div
      v-for="(project, idx) in projects"
      :key="idx"
      :style="{ 'grid-area': project.grid_area }"
      class="card"
    >
      <img class="preview_photo" :src="project.preview_url">
      <div class="card-description">
        <span class="card-label" v-text="project.label" />
        <span class="card-meta" v-text="project.meta" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      projects: [
        {
          label: 'Project Name 1',
          meta: 'Some Shit Here',
          grid_area: 'a',
          preview_url: require('~/assets/images/2020-06-11_Frame-16.JPG')
        },
        {
          label: 'Project Name 2',
          meta: 'Some Shit Here',
          grid_area: 'b',
          preview_url: require('~/assets/images/2020-06-11_Frame-16.JPG')
        },
        {
          label: 'Project Name 3',
          meta: 'Some Shit Here',
          grid_area: 'c',
          preview_url: require('~/assets/images/DSC07712.jpg')
        },
        {
          label: 'Project Name 4',
          meta: 'Some Shit Here',
          grid_area: 'd',
          preview_url: require('~/assets/images/IMG_8317-2.jpg')
        },
        {
          label: 'Project Name 5',
          meta: 'Some Shit Here',
          grid_area: 'e',
          preview_url: require('~/assets/images/IMG_8915-м.jpg')
        },
        {
          label: 'Project Name 6',
          meta: 'Some Shit Here',
          grid_area: 'e',
          preview_url: require('~/assets/images/IMG_8915-м.jpg')
        }
      ]
    }
  }
}
</script>

<style>
.band {
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 20px;
}

.card {
  background: white;
  width: 100%;
  height: 100%;
  position: relative;
}

.preview_photo {
  object-fit: cover;
  width: 100%;
  height: 100%;
  transition: filter .5s ease;
}

.preview_photo:hover {
  cursor: pointer;
  filter: brightness(75%);
}

.card-label {
  font-size: 32px;
  font-weight: 400;
  line-height: 1.2;
  letter-spacing: .01em;
  white-space: nowrap;
}

.card-description {
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #fff;
}

.card-meta {
  font-family: Noto Sans, sans-serif;
  font-size: 16px;
  font-weight: 100;
  line-height: 1.8em;
  letter-spacing: 0em;
}

@media only screen and (min-width: 500px) {
  .band {
    grid-template-columns: 1fr 1fr;
    grid-template-rows: repeat(3, 20em);
    grid-template-areas:
      "a b"
      "c d"
      "e f";
  }
}

@media only screen and (min-width: 850px) {
  .band {
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: repeat(4, 20em);
    grid-template-areas:
      "a a b"
      "a a c"
      "d f f"
      "e f f";
  }
}
</style>
