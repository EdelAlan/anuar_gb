<template>
  <div class="footer">
    <span class="footer-text" v-text="'© 2020'" />
    <span>Built by <a href="https://www.instagram.com/kaolines/" target="_blank" v-text="'kaolines'" /></span>
  </div>
</template>

<script>
export default {}
</script>

<style>

.footer {
  width: 100%;
  padding: 2.5em 0;
  height: max-content;
  display: flex;
  justify-content: space-between;
  align-items: center;

  font-family: Noto Sans, sans-serif;
  color: #727272;
  font-size: 15px;
  font-weight: 400;
  letter-spacing: 0em;
}

a {
  color: #727272;
  text-decoration: none;
  transition: all 250ms ease;
}

a:link {
  color: #727272;
}

a:visited {
  color: #727272;
}

a:hover {
  color: #ac0000;
}

a:active {
  color: #727272;
}

.header_buttons-link--active {
  text-decoration: underline;
}

@media only screen and (max-width: 500px) {
  .footer {
    flex-direction: column;
    align-items: center;
  }
  .footer-text {
    margin-bottom: .5em;
  }
}
</style>
