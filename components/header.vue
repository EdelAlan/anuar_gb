<template>
  <div class="header">
    <span class="header_label" v-text="'Anuar'" />
    <div class="header_buttons">
      <nuxt-link
        :class="{ 'header_buttons-link--active': isRouteSelected('index') }"
        class="header_buttons-link"
        to="/"
        v-text="'Home'"
      />
      <nuxt-link
        :class="{ 'header_buttons-link--active': isRouteSelected('gallery') }"
        class="header_buttons-link header_buttons-link-ml"
        to="/gallery"
        v-text="'Gallery'"
      />
      <nuxt-link
        :class="{ 'header_buttons-link--active': isRouteSelected('contacts') }"
        class="header_buttons-link header_buttons-link-ml"
        to="/contacts"
        v-text="'Contacts'"
      />
      <a class="icon-instagram" href="https://www.instagram.com/anuar_gb/" target="_blank" />
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    isRouteSelected (str) {
      return this.$route.name === str
    }
  }
}
</script>

<style>

.header {
  width: 100%;
  padding: 2.5em 0;
  height: max-content;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header_label {
  font-size: 27px;
  font-weight: 400;
}

.header_buttons {
  font-size: 18px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header_buttons-link {
  color: #272727;
  text-decoration: none;
}

.header_buttons-link:link {
  color: #272727;
}

.header_buttons-link:visited {
  color: #272727;
}

.header_buttons-link:hover {
  color: #ac0000;
}

.header_buttons-link:active {
  color: #272727;
}

.header_buttons-link--active {
  text-decoration: underline;
}

.header_buttons-link-ml {
  margin-left: 2em;
}

.icon-instagram {
  margin-left: 3em;
  cursor: pointer;
  width: 1.5em;
  height: 1.5em;
  background: url('~assets/icons/instagram.svg') center no-repeat;
}

@media only screen and (max-width: 500px) {
  .header {
    flex-direction: column;
    align-items: center;
  }
  .header_label {
    margin-bottom: .5em;
  }
  .header_buttons {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .icon-instagram {
    margin-left: 1em;
  }
  .header_buttons-link-ml {
    margin-left: 1em;
  }
}
</style>
