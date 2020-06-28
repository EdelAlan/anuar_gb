<template>
  <div class="container">
    <Header />
    <Nuxt />
  </div>
</template>

<style>
html {
  background-color: rgba(248,243,235,1);
  font-family: Playfair Display, serif;
  color: #272727;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  user-select: none;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.container {
  margin: 0 3.5em;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  text-align: center;
}
</style>
