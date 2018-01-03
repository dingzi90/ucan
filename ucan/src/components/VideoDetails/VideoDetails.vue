<template>
	<div class="VideoDetails">
			<div>
				<video   controls preload="auto"   poster="http://a.hiphotos.baidu.com/image/h%3D300/sign=b76869aca2ec8a130b1a51e0c7029157/c75c10385343fbf25255eb60bb7eca8065388f7c.jpg" >
					<source src="http://vjs.zencdn.net/v/oceans.mp4" type="video/mp4">
					<source src="http://vjs.zencdn.net/v/oceans.webm" type="video/webm">
					<source src="http://vjs.zencdn.net/v/oceans.ogv" type="video/ogg">
			 	</video>
			</div>
			<div class="lecturer">
				<p>主讲教师</p>
				<p ref="showtext">拥有超过8年教学经验的罗艺老师，在中考来临之际拥有超过8年教学经验的罗艺老师，在中考来临之际拥有超过8年教学经验的罗艺老师，在中考来临之际拥有超过8年教学经验的罗艺老师，在中考来临之际，为拥有超过8年教学经验的罗艺老师，在中考来临之际，为拥有超过8年教学经验的罗艺老师，在中考来临之际，为各位考生贡献的经典解题技巧分析汇总，大家觉得有用，请分享到朋友圈给更多的人看到！</p>
				<p @click="showAll" ref="showAll">显示全部</p>
				<div class="logoimg"><img src="~/common/images/img6.png"  /></div>
			</div>
			<div class="othersty">
				<h3>其他相关</h3>
				<ul>
					<li><img src="~/common/images/img5.png" /> 优能新晋英语大咖的有趣实验实践</li>
					<li><img src="~/common/images/img5.png" /> 优能最受学生欢迎英语教师</li>
				</ul>
			</div>
			<div  class="review">
				<h3>评论</h3>
				<ul>
					<li>
						<div class="name">
							<img  src="~/common/images/head.png"/>
							<p>少年与萌</p>
							<span class="floatRight">昨天 15:35</span>
						</div>
						<p class="reviewText">自从听了罗老师的课，英语成绩突飞猛进，老师讲的超级有趣哦！感觉很多枯燥的知识都变生动了，老师辛苦了！</p>
					</li>
					<li>
						<div class="name">
							<img  src="~/common/images/head.png"/>
							<p>少年与萌</p>
							<span class="floatRight">昨天 15:35</span>
						</div>
						<p class="reviewText">自从听了罗老师的课，英语成绩突飞猛进，老师讲的超级有趣哦！感觉很多枯燥的知识都变生动了，老师辛苦了！</p>
					</li>
				</ul>
			</div>
			<div class="discuss">
				  <p @click="alert">说点什么...</p>
			</div>
			<div class="discussAlert" ref="discussAlert">
				  <p><span class="floatRight send" @click="send">发送</span></p>
				  <div class="teatareaDiv"><textarea placeholder="说点什么..."></textarea></div>
			</div>
			<div class="demoDiv" ref="demoDiv"></div>
	</div>
</template>

<script type="text/ecmascript-6">
  export default {
    data() {
      return {
      }
    },
    methods: {
    	showAll(){
    		this.$refs.showtext.style.height = 'auto'
    		this.$refs.showAll.style.display = 'none'
    	},
    	alert() {
    		this.$refs.discussAlert.style.display = 'block'
    		this.$refs.demoDiv.style.display = 'block'
    	},
    	send() {
    		this.$refs.discussAlert.style.display = 'none'
    		this.$refs.demoDiv.style.display = 'none'
    	}
    }
  }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~common/stylus/reset"

	.VideoDetails
		width:100%
		overflow:hidden
		background:#fff
  .demoDiv
    position:fixed
    width:100%
    height:100%
    background:#000
    opacity:0.5
    z-index:98
    display:none
    left:0
    top:0
  .send
    padding:10px
	.discussAlert
	  position:fixed
	  bottom:0
	  height:165px
	  z-index:99
	  display:none
	  background:#fff
	  width:100%
	  p
	    height:40px
	    border-bottom:1px solid #ccc
	  .teatareaDiv
	   padding:15px
	   height:92px
	  textarea
	    width:100%
	    border:none
	    height:100%
	    outline:none
	    resize:none
	.discuss
	  position:fixed
	  bottom:0px
	  height:46px
	  width:100%
	  background:#fff
	  p
	    border-radius:34px
	    height:34px
	    width:80%
	    border:1px solid #ccc
	    margin:5px 5%
	    padding:0 5%
	    color:#999
	    line-height:34px
	.reviewText
	  font-size:14px
	  padding:10px 0px
	.review
	  padding:15px 15px 44px 15px
	  li
	    border-bottom:1px solid #e7e7e7
	  h3
	    font-size:18px
	    color:#333
	  .name
	    height:30px
	    line-height:30px
	    padding-top:5px
	    span
	      height:30px
	      line-height:30px
	      font-size:12px
	      color:#666
	    p
	      height:30px
	      line-height:30px
	      font-size:15px
	      float:left
	      padding-left:5px
	    img
	      height:30px
	      width:30px
	      border-radius:30px
	      float:left
	.othersty
		padding:15px
		h3
	    font-size:18px
	    color:#333
	  li
	    font-size:15px
	    color:#666666
	    img
	      width:9px
	      margin-bottom: 1px
	video
	  width:100%
	.logoimg
	  position:absolute
	  left:10%
	  top:-20px
	  z-index:2
	  background:#fff
	  padding:0 20px
	  img
	    width:35px
	.lecturer
		margin:15px
		position:relative
		border:3px solid #ddd
		p:nth-child(1)
		  height:35px
		  line-height:50px
		  font-size:18px
		  color:#333
		  text-align:center
		p:nth-child(2)
		  line-height:18px
		  font-size:15px
		  color:#999
		  text-align:left
		  padding:10px 20px
		  height:80px
		  overflow:hidden
		p:nth-child(3)
		  height:30px
		  line-height:30px
		  font-size:13px
		  color:#666666
		  text-align:center
		  background:#f0f0f0
</style>
