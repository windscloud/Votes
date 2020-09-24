/** 进度统计
 × 1. 查看所有部门的评测完成率。使用柱状图展示各个部门的统计进度：完成百分率，未完成人数
   2. 按时间查看， 时间/完成率的line (zhe-xian)
   3. 评测结束后，输出统计表格 部门/完成率/未完成人数/名字、名字、名字
 */
<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  }
}
</script>
