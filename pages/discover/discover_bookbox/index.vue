<template>
	<view class="content">
		<zyflow :flowlist="datalist" @flowtap="touchcard" @flowget="adddata" ></zyflow>
	</view>
</template>

<script>
	// 导入瀑布流组件
	import zyflow from "../../../components/zyflow/zyflow.vue"
	export default {
		//注册组件
		components:{
			zyflow
		},
		data() {
			return {
				datalist:[
			 {
			 	src:"../../static/发现页面/all/1.jpg",
			 	title:'很喜欢这种款式，很有设计感', 
			 	//showText:Math.floor(Math.random()+0.5)==1?true:false,
			 	showText:true,
			 	text:'您浏览过的足迹',
				showCity:true,
				city:'广州'
			 },
		 
				 {
					src:"../../static/发现页面/all/11.jpg",
					title:'价格真的是超便宜了，而且装纸也特别多，还不错', 
					//showText:Math.floor(Math.random()+0.5)==1?true:false,
					showText:true,
					text:'您浏览过的足迹',
					showCity:true,
					city:'郑州'
				 }, 
				{
					src:"../../static/发现页面/all/22.jpg",
					title:'抽纸盒也太可爱了吧，朋友来家里都以为是玩具', 
					//showText:Math.floor(Math.random()+0.5)==1?true:false,
					showText:true,
					text:'您浏览过的足迹',
					showCity:true,
					city:'宁波'
				},
					
					
					/* {
						src:"../../static/"+Math.floor(Math.random()*4+1)+".jpg",
						title:'春眠不觉晓,处处闻啼鸟.夜来风雨声,花落知多少', 
						showText:Math.floor(Math.random()+0.5)==1?true:false,
						text:'限时促销小助手为您推荐'
					},
					{
						src:"../../static/"+Math.floor(Math.random()*4+1)+".jpg",
						title:'寒雨连江夜入吴,平明送客楚山孤.洛阳亲友如相问,一片冰心在玉壶', 
						showText:Math.floor(Math.random()+0.5)==1?true:false,
						text:'限时促销小助手为您推荐'
					} */
				]
			}
		},
		onLoad() {
			
		},
		methods: {
			touchcard(e){
				/* console.log('点击此项获取到的数据')
				console.log(e);	 */
			},
			adddata(){
				console.log('调用增加数据函数');
				this.datalist = this.datalist.concat([{
						src:"../../static/发现页面/all/"+Math.floor(Math.random()*3+1)+".jpg",
						title:'春眠不觉晓,处处闻啼鸟.夜来风雨声,花落知多少',
				/* 		orig:Math.floor(Math.random()*1000),
						money:Math.floor(Math.random()*1000), */
						showText:Math.floor(Math.random()+0.5)==1?true:false,
						text:'您浏览过的足迹',
						showCity:Math.floor(Math.random()+0.5)==1?true:false,
						city:'上海'
					},
					{
						src:"../../static/发现页面/all/"+Math.floor(Math.random()*3+1)+".jpg",
						title:'寒雨连江夜入吴,平明送客楚山孤.洛阳亲友如相问,一片冰心在玉壶',
						/* orig:Math.floor(Math.random()*1000),
						money:Math.floor(Math.random()*1000), */
						showText:Math.floor(Math.random()+0.5)==1?true:false,
						text:'限时促销小助手为您推荐',
						showCity:Math.floor(Math.random()+0.5)==1?true:false,
						city:'义乌'
					},{
						src:"../../static/发现页面/all/"+Math.floor(Math.random()*3+1)+".jpg",
						title:'春眠不觉晓,处处闻啼鸟.夜来风雨声,花落知多少',
				/* 		orig:Math.floor(Math.random()*1000),
						money:Math.floor(Math.random()*1000), */
						showText:Math.floor(Math.random()+0.5)==1?true:false,
						text:'您浏览过的足迹',
						showCity:Math.floor(Math.random()+0.5)==1?true:false,
						city:'宁波'
					},
					{
						src:"../../static/发现页面/all/"+Math.floor(Math.random()*3+1)+".jpg",
						title:'寒雨连江夜入吴,平明送客楚山孤.洛阳亲友如相问,一片冰心在玉壶',
					/* 	orig:Math.floor(Math.random()*1000),
						money:Math.floor(Math.random()*1000), */
						showText:Math.floor(Math.random()+0.5)==1?true:false,
						text:'限时促销小助手为您推荐',
						showCity:Math.floor(Math.random()+0.5)==1?true:false,
						city:'金华'
					},{
						src:"../../static/发现页面/all/"+Math.floor(Math.random()*3+1)+".jpg",
						title:'春眠不觉晓,处处闻啼鸟.夜来风雨声,花落知多少',
					/* 	orig:Math.floor(Math.random()*1000),
						money:Math.floor(Math.random()*1000), */
						showText:Math.floor(Math.random()+0.5)==1?true:false,
						text:'您浏览过的足迹',
						showCity:Math.floor(Math.random()+0.5)==1?true:false,
						city:'深圳'
					},
					{
						src:"../../static/发现页面/all/"+Math.floor(Math.random()*3 +1)+".jpg",
						title:'寒雨连江夜入吴,平明送客楚山孤.洛阳亲友如相问,一片冰心在玉壶',
					/* 	orig:Math.floor(Math.random()*1000),
						money:Math.floor(Math.random()*1000), */
						showText:Math.floor(Math.random()+0.5)==1?true:false,
						text:'限时促销小助手为您推荐',
						showCity:Math.floor(Math.random()+0.5)==1?true:false,
						city:'郑州'
					}])
			}
		}
	}
</script>

<style>
	.content {
		width: 100%;
		height: 100%;
		position: absolute;
		background-color: #bfa;
	}
</style>
