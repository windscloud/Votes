/××
 × 3.2安排测试任务
 ×/
<template>
  <div class="home">
    <el-input></el-input>
    <el-input></el-input>
    <el-input></el-input>
    <el-input></el-input>
    <el-input></el-input>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  data() {
    return {
      id: -1, // 评测任务标识
      name: '', // 评测名称
      fileId: '', // 评测表文件Id, 不显示
      fileName: '', // 评测表文件名
      dateCreated: '', //创建日期，自动生成
      dateStart: '', //评测开始日期, input
      dateEnd: '', //评测结束日期, input
    }
  }
}
</script>
