<template>
	<div class="Content">
		<div>
			<div class="container">
				<div class="row contentBlock contentBg" style="">
					<div class="content-title">
						<h2><b>Welcome</b></h2>
						<p>Here, you will find somethings which are fun and interesting</p>
						<p>I hope you will enjoy it, have fun! </p>
					</div>
				</div>
				<div class="row contentBlock contentBgTwo">
					<div class="col-xs-12 col-sm-12 col-md-4">
						<div class="smallBox">
							<a href="/#"><img src="../../static/images/flowers/23.png" alt="" height="270px" width="340px"></a>
							<span class="smallBox-tips">
								Here, you will find somethings which are fun and interestingHere, you will find somethings which are fun and interestingHere, you will find somethings which are fun and interesting
							</span>
						</div>
					</div>
					<div class="col-xs-12 col-sm-6 col-md-4">
						<div class="smallBox">
							<a href="/#"><img src="../../static/images/flowers/25.png" alt="" height="270px" width="340px"></a>
							<span class="smallBox-tips">news</span>
						</div>
					</div>
					<div class="col-xs-12 col-sm-6 col-md-4">
						<div class="smallBox">
							<a href="/#"><img src="../../static/images/flowers/22.png" alt="" height="270px" width="340px"></a>
							<span class="smallBox-tips">news</span>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Content',
	data () {
		return {

		}
	},
	mounted () {

	}
}
</script>
<style>
	*{
		margin: 0;
		padding: 0;
	}
	.content{
		color:#fff;
	}
	.contentBlock{
		margin: 50px 0;
		/*padding: 30px 0;*/
		width: 100%;
		height: 450px;
		text-align: center;
		/*box-sizing: border-box;*/
	}
	.contentBg{
		background: #66ccFF33;
	}
	.contentBgTwo{
		background: #ffffff99;
	}
	.content-title{
		position: relative;
		top: 50%;
		/*top:calc(50% - 66px);*/
		font-family: 'Microsoft Yahei';
		font-size: 28px;
		font-weight: bold;
		vertical-align:middle;
		transform:translateY(-50%);
		-webkit-transform:translateY(-50%);
		/*color: #EE5500AA;*/
	}
	.smallBox{
		margin:30px 0;
	}
	.smallBox .smallBox-tips{
		margin-top: 15px;
		display: block;
		height: 120px;
		line-height: 24px;
		overflow: hidden;
	}
</style>
