/** 结果统计
 × 1. 查看所有部门的评测结果。查看职工的投票情况。学院：用条形图展示每个职工对所有领导干部的评分,职工匿名
 × 2. 查看所有部门的被评测结果。查看领导的得分情况。学院：用条形图展示每个职工对所有领导干部的评分,职工匿名
   3. 表格展示上述领导的得分情况：领导名字/平均得分/最高给分/最低给分/优秀数/良好/一般/差/方差
   4. 每个领导单独显示各项得分情况。条形图，坐标是测评item，系列为测评等级（优秀/良好/一般/差）,数值为得票数
   5. 全校的统计，用条形图，展示各个学院、各个领导的平均分
   6. 全校的统计，用表格，展示各个学院、各个领导的平均分
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
