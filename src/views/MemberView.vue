<template>
  <div class="home">
    <el-button type="primary" @click="nextPage">next</el-button>
    {{index}}
    {{rowObj}}
  <el-table
        :data="tableData"
        style="width: 100%">
        <el-table-column
          prop="date"
          label="工号"
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
import {members} from '../store/members'

export default {
  name: 'members',
  computed: {
    tableData() {
      let d = new Array()
      for(let i=this.from; (i<this.from+this.num) && i<members.length; i++){
        d.push(members[i])
      }
      return d
    }
  },
  mounted() {
    this.total = members.length/this.num+1
  },
  methods: {
    nextPage(){
      this.from = this.from+this.num
    },
    prevPage() {
      this.from = this.from+this.num
    },
    filter(dept){
      let temp = members.filter(function(elem){return elem.address===dept})
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
      num: 2,
      total: -1,
      index: -1,
      rowObj: null
    }
  }
}
</script>
