<template>
	<div class="Hamlet">
		<scroll :data="data"
				:pullup="pullup"
	  			:beforeScroll="beforeScroll"
          		@beforeScroll="listScroll">
        	<div class="list">
	        	<ul>
	        		<li>
	        			<dl>
	        				<dt><img src="~/common/images/img2.png" /></dt>
	        				<dd>
	        					<p>优能中学大咖数学老师——祝林骏21世纪杯英语演讲初中组赛培讲座</p>
	        					<div class="infor">
	        						<img src="~/common/images/img3.png"  />
	        						<span>19.2万</span>
	        						<span class="floatRight">2017.10.09</span>
	        					</div>
	        				</dd>
	        			</dl>
	        		</li>
	        		<li>
	        			<dl>
	        				<dt><img src="~/common/images/img2.png" /></dt>
	        				<dd>
	        					<p>优能中学大咖数学老师——祝林骏21世纪杯英语演讲初中组赛培讲座</p>
	        					<div class="infor">
	        						<img src="~/common/images/img3.png"  />
	        						<span>19.2万</span>
	        						<span class="floatRight">2017.10.09</span>
	        					</div>
	        				</dd>
	        			</dl>
	        		</li>
	        		<li>
	        			<dl>
	        				<dt><img src="~/common/images/img2.png" /></dt>
	        				<dd>
	        					<p>优能中学大咖数学老师——祝林骏21世纪杯英语演讲初中组赛培讲座</p>
	        					<div class="infor">
	        						<img src="~/common/images/img3.png"  />
	        						<span>19.2万</span>
	        						<span class="floatRight">2017.10.09</span>
	        					</div>
	        				</dd>
	        			</dl>
	        		</li>
	        		<li>
	        			<dl>
	        				<dt><img src="~/common/images/img2.png" /></dt>
	        				<dd>
	        					<p>优能中学大咖数学老师——祝林骏21世纪杯英语演讲初中组赛培讲座</p>
	        					<div class="infor">
	        						<img src="~/common/images/img3.png"  />
	        						<span>19.2万</span>
	        						<span class="floatRight">2017.10.09</span>
	        					</div>
	        				</dd>
	        			</dl>
	        		</li>
	        		<li>
	        			<dl>
	        				<dt><img src="~/common/images/img2.png" /></dt>
	        				<dd>
	        					<p>优能中学大咖数学老师——祝林骏21世纪杯英语演讲初中组赛培讲座</p>
	        					<div class="infor">
	        						<img src="~/common/images/img3.png"  />
	        						<span>19.2万</span>
	        						<span class="floatRight">2017.10.09</span>
	        					</div>
	        				</dd>
	        			</dl>
	        		</li>
	        		<li>
	        			<dl>
	        				<dt><img src="~/common/images/img2.png" /></dt>
	        				<dd>
	        					<p>优能中学大咖数学老师——祝林骏21世纪杯英语演讲初中组赛培讲座</p>
	        					<div class="infor">
	        						<img src="~/common/images/img3.png"  />
	        						<span>19.2万</span>
	        						<span class="floatRight">2017.10.09</span>
	        					</div>
	        				</dd>
	        			</dl>
	        		</li>
	        	</ul>
	        </div>
		</scroll>
	 	<div class="loading-container" v-show="showFlag">
        	<loading></loading>
      	</div>
	</div>
</template>

<script type="text/ecmascript-6">
  	import Scroll from 'base/scroll/scroll'
	import Loading from 'base/loading/loading'
  export default {
    data() {
      return {
        showFlag: false,
        pullup: true,
  		beforeScroll: true,
  		data:[1,2]
      }
    },
    created() {
	    this.probeType = 3
	    this.listenScroll = true
	},
    methods: {
    	listScroll() {
	        this.$emit('listScroll')
	    }
    },
    components: {
      Scroll,
      Loading
    }
  }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~common/stylus/reset"

	.Hamlet
		width:100%
		overflow:hidden
		background:#fff
	.list li
	    height:100px
	    width:100%
	    dl
	        display:flex
	        padding:15px 15px 0 15px
	        dt
	            width:85px
	            img
	                width:70px
	                height:70px
	        dd
	        	flex:1
	        	border-bottom:1px solid #e7e7e7
	        	position:relative
	        	padding-bottom:30px
	        	height:55px
	        	p
	        		font-size:15px
	        		line-height:18px
	        	.infor
	        		height:18px
	        		position:absolute
	        		bottom:15px
	        		width:100%
	        		img
	        			width:10px
	        			margin-bottom:-1px
	        		span
	        		    font-size:12px
	        		    color:#999
	        		    line-height:28px
	        		    height:18px
</style>