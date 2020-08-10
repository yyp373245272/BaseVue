<template>
	<div id="app">
		<el-container>
			<el-header>
				<p>123</p>
			</el-header>
			<el-container>
				<el-aside>
					<side-bar/>
				</el-aside>
				<el-main>
					<router-view />
				</el-main>
			</el-container>
		</el-container>
	</div>
</template>

<style>
#app {
  font-family: "Source Sans Pro", "Helvetica Neue", Arial, sans-serif;
  text-align: center;
}
.el-header {
  position: relative;
  -webkit-app-region: drag;
  text-align: left;
  background-color: #00dfc1;
  color: rgb(255, 0, 0);
  margin: 0;
}
</style>

<script>
import SideBar from './components/SiderBar.vue'
export default {
	components: {
		SideBar
	}
}
</script>
