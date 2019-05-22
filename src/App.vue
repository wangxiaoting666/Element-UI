<template>
  <div>
   <el-col :span="2">   
    <el-menu
      :default-active="this.$route.path" 
      router mode="horizontal"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b">
      <el-menu-item v-for="(item,i) in navList" :key="i" :index="item.name">
        <template slot="title">
          <i class="el-icon-eleme"></i>
          <span> {{ item.navItem }}</span>
        </template>

      </el-menu-item>
       
        
    </el-menu>
  </el-col>
  
  <router-view     class="menu-right"/>

  </div>
</template>
<script>
  export default {
  	data() { 
  		return { 
  			navList:[ 
  			{name:'/components/ServiceHall',navItem:'服务大厅'}, 
  			{name:'/components/Management',navItem:'权限管理'},
  			{name:'/components/User',navItem:'用户管理'}, 
  			{name:'/components/Personnel',navItem:'人员数据'}, 
  			{name:'/components/Alarm',navItem:'报警中心'}, 
  			
  			{name:'/components/Asset',navItem:'资产中心'},
  			{name:'/components/Map',navItem:'地图中心'},
  			
  			] } 
  	},
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>

<style>
	.menu-right{
		margin-left:200px;
	}
	
</style>