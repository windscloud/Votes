/×× 在web打开excel文档
 ×/
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
          label="文件名"
          width="180">
        </el-table-column>
    <el-table-column label="操作">
      <template slot-scope="scope">
        <el-button
          icon="el-icon-download"
          size="mini"
          @click="handleEdit(scope.$index, scope.row)">下载</el-button>
        <el-button
          icon="el-icon-delete" 
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
import {evals} from '../store/evals'

export default {
  name: 'evals',
  computed: {
    tableData() {
      let d = new Array()
      for(let i=this.from; (i<this.from+this.num) && i<evals.length; i++){
        d.push(evals[i])
      }
      return d
    }
  },
  mounted() {
    this.total = evals.length/this.num+1
  },
  methods: {
    nextPage(){
      this.from = this.from+this.num
    },
    prevPage() {
      this.from = this.from+this.num
    },
    filter(dept){
      let temp = evals.filter(function(elem){return elem.address===dept})
      window.console.log(temp)
    },
    handleEdit(index, row) {
      this.index = index
      this.rowObj = row
    }
  },
  data() {
    return {
      // tableData:[],
      from: 0,
      num: 20,
      total: -1,
      index: -1,
      rowObj: null
    }
  }
}
</script>
