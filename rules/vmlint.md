## VM Lint规则 [via](http://doc.alipay.net/pages/viewpage.action?pageId=33063036)
- （1级）系统静态文件命名需符合规范
	* system/system.prod-version.(js|css) 
如：[https://a.alipayobjects.com/personal/personal.i-1.6.js] 
 	* ar/开头的 
如：[https://a.alipayobjects.com/ar/arale.core-1.1.js] 
	* al/开头的 
如：[https://a.alipayobjects.com/al/alice.style.account-1.1.css] 
	* build/开头的 
如：https://a.alipayobjects.com/build/js/arale.js
- （1级）系统静态文件及uisvr目录结构规范
	* /static 
	* /static/js 
	* /static/css 
	* /(system-)htdocs 
	* /(system-)htdocs/template 
	* /(system-)htdocs/uisvr 
	* /(system-)htdocs/uisvr/config 
	* /(system-)htdocs/uisvr/config/system.properties 
	* /(system-)htdocs/uisvr/config/js.vm 
	* /(system-)htdocs/uisvr/config/css.vm 
	* /(system-)htdocs/uisvr/config/config.xml 
	* /(system-)htdocs/uisvr/theme	
- （1级）不使用其他系统的静态文件 
	- 比如personal使用personalprod.prodhome-1.0.css 
避免造成后续的系统发布依赖等问题

- （1级）vm文件(template和uisvr)编码需为gbk，静态文件(js/css)需为utf-8	 
- （1级）静态文件的引用，没有直接写“*-SNAPSHOT"
- （1级）页面里不应存在alipay.net的硬编码。检测规则为：[http://*.(png]
- （2级）不能直接用==做变量判断，如变量为 null 会报错
	- 正确写法：$stringUtil.equals($a,"1")
- （2级）screen及tile目录下的单个vm文件内标签建议闭合
- 前端tile目录结构规范，js及css的公用tile（如有），请放置以下目录： 
	* /(system-)htdocs/uisvr/tile-js 
	* /(system-)htdocs/uisvr/tile-css	 
- （2级）使用变量时使用$! 非$，如果变量为 null，那么页面会直接显示该变量 $a




## 其他参考资料
- [前端持续集成](http://doc.alipay.net/pages/viewpage.action?pageId=33523099#%E5%89%8D%E7%AB%AF%E6%8C%81%E7%BB%AD%E9%9B%86%E6%88%90-monsterlint%E7%9A%84%E7%BB%84%E6%88%90)
- [Google HTML/CSS Style Guide](http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml)
- [W3C Quality Tools](http://www.w3.org/QA/Tools/)