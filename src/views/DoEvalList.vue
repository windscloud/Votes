/**职工浏览测评任务 */
<template>
  <div class="home">
  <el-table
        :data="tableData"
        style="width: 100%">
        <el-table-column
          prop="date"
          label="序号"
          width="180">
        </el-table-column>
        <el-table-column
          prop="name"
          label="处级干部"
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
        <el-table-column
          prop="dateStart"
          label="开始日期">
        </el-table-column>
        <el-table-column
          prop="dateEnd"
          label="结束日期">
        </el-table-column>
    <el-table-column label="操作">
      <template slot-scope="scope">
        <el-button
          size="mini"
          @click="handleEdit(scope.$index, scope.row)">测评</el-button>
        <el-button
          size="mini"
          type="danger"
          @click="handleDelete(scope.$index, scope.row)">提交</el-button>
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
  components: {
    HelloWorld
  }
}
</script>
