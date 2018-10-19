<template>
  <div>
    <nuxt/>
  </div>
</template>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #00bfb2;
  color: #00bfb2;
  text-decoration: none;
  padding: 10px 30px;
  margin: 4px 8px;
}

.button--green:hover {
  color: #fff;
  background-color: #00bfb2;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin: 4px 8px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.button--blue {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #327bc9;
  color: #327bc9;
  text-decoration: none;
  padding: 10px 30px;
  margin: 4px 8px;
}

.button--blue:hover {
  color: #fff;
  background-color: #327bc9;
}

.social {
  padding-top: 15px;
}

.social a {
  padding: 10px;
  border-bottom: 2px solid transparent;
  display: inline-block;
}

.social a:hover {
  border-color: #00bfb2;
}

.social img {
  height: 24px;
}
</style>
