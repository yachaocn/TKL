#PULL REQUEST - Write to kieran

1.添加 /layout/casper/after_all.ejs加入如下代码：实现侧边栏百度分享功能[百度分享](http://share.baidu.com/code)

	
	<script>window._bd_share_config={"common":{"bdSnsKey":	{},"bdText":"","bdMini":"2","bdMiniList":false,"bdPic":"","bdStyle":"2","bdSize":"16"},"slide":	{"type":"slide","bdImg":"7","bdPos":"right","bdTop":"100"},"image":{"viewList":	["qzone","tsina","tqq","renren","weixin"],"viewText":"分享到：","viewSize":"16"},"selectShare":	{"bdContainerClass":null,"bdSelectMiniList":	["qzone","tsina","tqq","renren","weixin"]}};with(document)0[(getElementsByTagName('head')[0]||	body).appendChild(createElement('script')).src='http://bdimg.share.baidu.com/static/api/js/share.js?	v=89860593.js?cdnversion='+~(-new Date()/36e5)];</script>
	

---

2.在/layout/casper/新建google_analytics.ejs加入如下代码实现GoogleAnalytics网站分析统计。 配置文件加入google_analytics

	<% if (theme.google_analytics){ %>
	<script>
 	 (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
 	 (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
 	 m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
 	 })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
    ga('create', ‘<%= theme.google_analytics %>’, 'auto');
  	ga('send', 'pageview');
	</script>
	<<% } %>
	
3.添加 /layout/post.ejs加入如下代码：实现[Fork me on github](https://github.com/blog/273-github-ribbons)
	
	<a href="<%= theme.github %>"><img style="position: absolute; top: 0; left: 0; border: 0;" src="https://camo.githubusercontent.com/82b228a3648bf44fc1163ef44c62fcc60081495e/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f6c6566745f7265645f6161303030302e706e67" alt="Fork me on GitHub" data-canonical-src="https://s3.amazonaws.com/github/ribbons/forkme_left_red_aa0000.png"></a>
	
