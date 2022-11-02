<template>
  <div class="test__wrapper">
    <div class="test">TESTページ</div>
  </div>
</template>

<style scoped>
.test__wrapper {
  padding: 3rem;
  background: #000;
}
.test {
  position: relative;
  width: 300px;
  height: 300px;
  border-radius: 30px;
  background: #000;
}
.test::before {
  box-sizing: border-box;
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  content: '';
  border-radius: 28px;
  padding: 2px;
  width: 100%;
  background-size: 400% auto;
  background-position: 0 0;
  opacity: 0.5;
  transition: background-position 0.3s ease-in-out, opacity 0.2s ease-in-out;
  -webkit-mask: linear-gradient(#fff 0 0);
  mask: linear-gradient(#fff 0 0);
  background-image: linear-gradient(90deg, #303030 0%, #303030 25%, #00DC82 50%, #36E4DA 75%, #0047E1 100%);
  border-width: 0;
  border-style: solid;
  border-color: #e5e7eb;
  -webkit-mask-composite: xor;
  mask-composite: exclude;
  -webkit-mask-clip: content-box, initial;
  mask-clip: content-box, initial;
}
.test:hover::before {
  background-position: -50% 0;
  opacity: 1;
}
</style>