<template>
  <div class="band">
    <div
      v-for="(project, idx) in projects"
      :key="idx"
      :style="{
        'grid-area': project.grid_area,
        'background-image': `url(${project.preview_url})`
      }"
      class="card"
    >
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
          label: 'Project 1',
          meta: 'beauty',
          grid_area: 'a',
          preview_url: require('~/assets/images/3.jpg')
        },
        {
          label: 'Project 2',
          meta: 'film',
          grid_area: 'b',
          preview_url: require('~/assets/images/2020-06-11_Frame-16.JPG')
        },
        {
          label: 'Project 3',
          meta: 'travel',
          grid_area: 'c',
          preview_url: require('~/assets/images/DSC07712.jpg')
        },
        {
          label: 'Project 4',
          meta: 'travel',
          grid_area: 'd',
          preview_url: require('~/assets/images/IMG_8317-2.jpg')
        },
        {
          label: 'Project 5',
          meta: 'wedding',
          grid_area: 'e',
          preview_url: require('~/assets/images/IMG_0172-2.jpg')
        },
        {
          label: 'Project 6',
          meta: 'beauty',
          grid_area: 'f',
          preview_url: require('~/assets/images/MasterClass_Day20268-3V.jpg')
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
  cursor: pointer;
  transition: filter .5s ease;
  background-size: cover;
  background-repeat: no-repeat;
}

.card:hover > .card-description {
  color: #000;
}

.card:hover {
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
  cursor: pointer;
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  bottom: .5em;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #fff;
  transition: all .5s ease;
}

.card-meta {
  font-family: Noto Sans, sans-serif;
  font-size: 16px;
  font-weight: 100;
  line-height: 1.8em;
  letter-spacing: 0em;
}

@media only screen and (max-width: 500px) {
  .band {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(6, 20em);
    grid-template-areas:
      "a"
      "b"
      "c"
      "d"
      "e"
      "f";
  }
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
