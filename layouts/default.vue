<template>
  <div>
    <nuxt/>
  </div>
</template>

<style>
/* @import url('https://fonts.googleapis.com/css?family=Dosis|Sawarabi+Mincho'); */
/* @import url('https://fonts.googleapis.com/css?family=Khand:400,500,600,700'); */
@import url('https://fonts.googleapis.com/css?family=Chakra+Petch:500,600,700|Ubuntu+Mono:400,700');

html {
  font-family: 'Chakra Petch', sans-serif;
  /* font-family: 'Ubuntu Mono', monospace; */
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
