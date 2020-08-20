<template>
  <div class="container">
    <div class="header">标题头</div>
    <div>
      <nuxt-child />
    </div>
    <div class="bottom">底部</div>
  </div>
</template>

<script>
export default {};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.header,
.bottom {
  width: 100%;
  height: 50px;
  background: green;
  position: fixed;
  left: 0;
  top: 0;
}
.bottom {
  top: auto;
  bottom: 0;
}
</style>
