/××
 × 3.2安排测试任务
 ×/
<template>
  <div class="home">
  <el-table
        :data="tableData"
        style="width: 100%">
        <el-table-column
          prop="name"
          label="任务名"
          width="180">
        </el-table-column>
        <el-table-column
          prop="name"
          label="姓名"
          width="180">
        </el-table-column>
        <el-table-column
          prop="address"
          label="部门">
        </el-table-column>
        <el-table-column
          prop="title"
          label="职务">
        </el-table-column>
    <el-table-column label="操作">
      <template slot-scope="scope">
        <el-button
          size="mini"
          @click="handleEdit(scope.$index, scope.row)">分配</el-button>
        <el-button
          size="mini"
          @click="handleEdit(scope.$index, scope.row)">编辑</el-button>
        <el-button
          size="mini"
          type="danger"
          @click="handleDelete(scope.$index, scope.row)">删除</el-button>
      </template>
    </el-table-column>        
  </el-table>
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
      file: '', // 评测表文件名
      dateCreated: '', //创建日期，自动生成
      dateStart: '', //评测开始日期, input
      dateEnd: '', //评测结束日期, input
    }
  }
}
</script>
