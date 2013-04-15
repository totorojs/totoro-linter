## CSSLint规则集 [via](https://github.com/stubbornella/csslint/wiki/Rules#noahludev)
CSS的校验，使用开源的CSSLint进行代码的校验。包含的规则可以参考：CSSLint Rules。  
The following rules point out potential errors in your CSS.

- Beware of box model size
- Require properties appropriate for display
- Disallow duplicate properties
- Disallow empty rules
- Require use of known properties

针对支付宝前端的代码规范，特别新增的校验规则有：

- 不能使用不规范的图片URL
- 不能使用相对地址
- 不能使用测试环境的地址
- 只能使用支付宝线上服务器URL，比如可以使用https://i.alipayobjects.com/a.png , 当不能使用 https://taobao.com/a.png