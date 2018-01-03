<template>
	<div class="OptimizingAudioVisual">
		<scroll :data="data"
				:pullup="pullup"
	  			:beforeScroll="beforeScroll"
          		@beforeScroll="listScroll">
		 	<div v-if="!showFlag" class="slider-wrapper" ref="sliderWrapper">
	          <slider>
		          	<div>
		              	<a href="/hello">
		                	<img class="needsclick"  src="~/common/images/img1.png">
		              	</a>
	                </div>
	                	<div>
		              	<a href="/hello">
		                	<img class="needsclick"  src="~/common/images/img1.png">
		              	</a>
	                </div>
	                	<div>
		              	<a href="/hello">
		                	<img class="needsclick"  src="~/common/images/img1.png">
		              	</a>
	                </div>
	          </slider>
	        </div>
	        <div class="tab">
	        	<div @click="tab(1)"><span :class="{tabTrue:istab1}" ref="tab1">最新</span></div>
	        	<div @click="tab(2)"><span :class="{tabTrue:istab2}" ref="tab2">最热</span></div>
	        </div>
        	<div class="list" ref="list1">
	        	<ul>
	        		<li>
	        			<dl>
	        				<dt><img src="~/common/images/img2.png" /></dt>
	        				<dd>
	        					<p>优能中学大咖数学老师——祝林骏21世纪杯英语演讲初中组赛培讲座</p>
	        					<div class="infor">
	        						<img src="~/common/images/invalidName@2x.png"  />
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
	        						<img src="~/common/images/invalidName@2x.png"  />
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
	        						<img src="~/common/images/invalidName@2x.png"  />
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
	        						<img src="~/common/images/invalidName@2x.png"  />
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
	        						<img src="~/common/images/invalidName@2x.png"  />
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
	        						<img src="~/common/images/invalidName@2x.png"  />
	        						<span>19.2万</span>
	        						<span class="floatRight">2017.10.09</span>
	        					</div>
	        				</dd>
	        			</dl>
	        		</li>
	        	</ul>
	        </div>
	        <div class="list" ref="list2">
	        	<ul>
	        		<li>
	        			<dl>
	        				<dt><img src="~/common/images/img2.png" /></dt>
	        				<dd>
	        					<p>优能中学大咖数学老师——祝林骏21世纪杯英语演讲初中组赛培讲座</p>
	        					<div class="infor">
	        						<img src="~/common/images/invalidName@2x.png"  />
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
	import Slider from 'base/slider/slider'
	import Loading from 'base/loading/loading'
  export default {
    data() {
      return {
        showFlag: false,
        refreshDelay: 120,
        pullup: true,
  		beforeScroll: true,
  		istab1: true,
  		istab2: false,
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
	   },
	   tab(n) {
	   		if(n === 1){
	   			this.istab1 = true
	   			this.istab2 = false
	   			this.$refs.list1.style.display = 'block'
	   			this.$refs.list2.style.display = 'none'
	   		}else{
	   			this.istab1 = false
	   			this.istab2 = true
	   			this.$refs.list2.style.display = 'block'
	   			this.$refs.list1.style.display = 'none'
	   		}
	   }
    },
    components: {
      Scroll,
      Slider,
      Loading
    }
  }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~common/stylus/reset"

	.OptimizingAudioVisual
		width:100%
		overflow:hidden
		background:#fff
	.tab
	    height:48px
	    border-bottom:1px solid #e7e7e7
	    div
	        float:left
	        width:50%
	        text-align:center
	        span
	        	line-height:48px
	        	display:inline-block
	        	height:40px
	        	color:#333
	        .tabTrue
	         	border-bottom:3px solid #fbe037
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
	        			width:7px
	        			margin-bottom:-1px
	        		span
	        		    font-size:12px
	        		    color:#999
	        		    line-height:28px
	        		    height:18px
</style>