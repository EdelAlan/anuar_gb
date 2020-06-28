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
        class="header_buttons-link ml-2"
        to="/gallery"
        v-text="'Gallery'"
      />
      <nuxt-link
        :class="{ 'header_buttons-link--active': isRouteSelected('contacts') }"
        class="header_buttons-link ml-2"
        to="/contacts"
        v-text="'Contacts'"
      />
      <a class="icon-instagram ml-3" href="https://www.instagram.com/anuar_gb/" target="_blank" />
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
  padding: 1.5em 0;
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

.ml-2 {
  margin-left: 2em;
}

.ml-3 {
  margin-left: 3em;
}

.icon-instagram {
  cursor: pointer;
  width: 1.5em;
  height: 1.5em;
  background: url('~assets/icons/instagram.svg') center no-repeat;
}
</style>
