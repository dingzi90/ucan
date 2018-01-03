<template>
	<div class="KUTest">
		<div class="kuTestStart">
			<h3>通过你喜爱的科目测试未来职业方向</h3>
			<div class="infor">
				<span>2017-10-16</span>
				<span>清韵</span>
				<span>优能U学堂</span>
			</div>
			<div class="TextLogo">
				<img  src="~/common/images/img4.png"  />
				<p>"我性格内向/外向，适合什么工作？”“哪些职
					业正好匹配我的性格？”“以我的个性从事什么
					行业好？”“我性格中的优势和劣势是什么？”
					“我是不是该继续现在从事的职业？”</p>
			</div>
			<div class="count">
				<div class="floatRight" >
					<img src="~/common/images/img3.png"  />
					<span>9.2万</span>
				</div>
			</div>
			<div class="button">立即测试</div>
		</div>
	</div>
</template>

<script type="text/ecmascript-6">
  export default {
    data() {
      return {
      }
    }
  }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~common/stylus/reset"

	.KUTest
		width:100%
		overflow:hidden
		background:#fff
	.button
	  margin:30px 20px
	  border-radius:5px
	  height:45px
	  line-height:45px
	  background:#fbe037
	  color:#333
	  text-align:center
	.count
	  height:30px
	  img
	    width:10px
	  span
	    font-size:12px
	    color:#999
	.TextLogo
	   padding:20px
	   img
	     width:100%
	.kuTestStart
	  padding:15px
	  h3
	    font-size:25px
		.infor
		  span:nth-child(1)
		    font-size:18px
		    color:#888
		  span:nth-child(2)
		    font-size:18px
		    color:#888
		  span:nth-child(3)
		    font-size:18px
		    color:#576b95
</style>