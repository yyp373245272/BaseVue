<template>
    <div>
        <el-col :span="18" id="sideBar">
            <el-button id="addBtn" type="primary" icon="el-icon-edit" circle @click='additem()'></el-button>
            <el-menu router mode="vertical" >
                <el-menu-item index="/" v-for="(item,i) in this.sheetlist" :key="item" ><i class="el-icon-document"></i>{{ item }}</el-menu-item>
                <el-menu-item index="/"><i class="el-icon-document"></i>sheet2</el-menu-item>
                <el-menu-item index="/"><i class="el-icon-document"></i>sheet2</el-menu-item>
            </el-menu>
        </el-col>
    </div>
</template>

<script>
export default {
  name: 'SiderBar',
  data () {
    return {
      msg: ['Welcome to Your Vue.js App'],
      sheetcount: 0,
      sheetlist: []
    }
  },
  methods: {
      additem: function () {
          var item = 'sheet1'
          this.sheetcount++
          this.sheetlist.push(item) 
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
#sideBar {
  height: 100%;
  text-align: left;
}
</style>
