<template>
  <div>
    <h2>这是一个vue的使用示例</h2>
    <img src="../assets/img/jpg1.jpg" width="100" alt="">

    <h2>style使用示例</h2>
    <div class="red">sass</div>
    <div class="pink">scoped</div>
    <div :class="$style.blue">css module + sass变量</div>
    <div class="green">src外链</div>

    <h2>render函数 + jsx & pug</h2>
    <Test></Test>
    <Test2></Test2>
  </div>
</template>

<script>
import Test from './Test';
import Test2 from './Test2';

export default {
  name: 'HelloWorld',
  components: {
    Test,
    Test2,
  },
  data() {
    return {};
  }
};
</script>

<style lang='scss'>
.red {
  color: red;
}
</style>

<style lang='scss' scoped>
.pink {
  color: pink;
}
</style>

<style lang='scss' module>
.blue {
  color: blue;
}
</style>

<style lang='scss' src="./HelloWorld.scss"></style>