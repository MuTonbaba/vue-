<template>
	
  <div id="app">
		<input type="text" v-model="text">
		<button @click="shanchu">按钮</button>
		<ul>
			<li v-for="(a,index) in list" :key="index" @click="asd(index)">
				{{a}}
			</li>
		</ul>
  </div>
	
</template>

<script>
	export default{
		data(){
			return({
				list:[
					"mubaba",
					"muyeye",
					"蔡徐坤"
				],
				text:''
			})
			
		},
		methods:{
			shanchu(){
				this.list.push(this.text);
				this.text=""
			},
			asd(index){
				this.list.splice(index,1)
			}
		}
	}
</script>

<style>
		li{
			list-style-type: none;
		}
		#app{
			margin: 0 auto;
			width: 220px;
			height: auto;
			background: rgb(255, 255, 255);
			border: 1px solid rgb(199, 17, 17);
		}
		input{
			background: rgb(255, 255, 255);
		}
		button{
			background: rgb(255, 0, 0);
			color: white;
		}
		 li{
			border-bottom: 1px solid rgb(255, 255, 255);
		}
		
</style>