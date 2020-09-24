/××
 × 3.2分配测评任务
 ×/
<template>
  <div class="home">
    {{name}}, {{dateBegin}}, {{dateEnd}}}
    <el-table
    ref="multipleTable"
    :data="tableData"
    tooltip-effect="dark"
    style="width: 100%"
    @selection-change="handleSelectionChange">
    <el-table-column
      type="selection"
      width="55">
    </el-table-column>
    <el-table-column
      prop="deptName"
      label="部们"
      width="120">
    </el-table-column>
  </el-table>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  methods: {
    dispatch() {
      window.console.log('.......')
    }
  },
  data() {
    return {
      id: -1, // 评测任务标识
      name: '', // 评测名称
      fileId: '', // 评测表文件Id, 不显示
      fileName: '', // 评测表文件名
      dateCreated: '', //创建日期，自动生成
      dateStart: '', //评测开始日期, input
      dateEnd: '', //评测结束日期, input
      tableData: [{id: 0, deptName:'计算机学院'},{id:2, deptName:'国脚学院'}]
    }
  }
}
</script>
