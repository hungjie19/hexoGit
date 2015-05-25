title: 'coServ workshop #05 淺談Sass + RWD'
date: 2015-05-21 19:06:46
tags:
- coServ
- workshop
- nodeJS
---

![coServ workshop #05](https://googledrive.com/host/0B4fEFbbW93y5XzJtbHZJX09qNGs)

<!--more-->

# 1、coServ JASS
[講者投影片 YyuchenY](http://www.slideshare.net/YyuchenY/jass-in-coserv-48462059)

* Just Awesome Style Sheet 
	* 與 Sass 類似，也可以寫 Sass
	* 變數、巢狀迴圈、Mixins(混用/函式)、擴充(繼承)
	* 不需另外學一套語法
	* 直接以 JavaScript 實作

#### Mixins(混用/函式):

``` css
function borderRadius(radius)  {
		//radius = parseInt(radius)*0.2+'px'
		return  {
			'-webkit-border-radius': radius,
			'-moz-border-radius': radius,
			'-ms-border-radius': radius,
			'border-radius': radius
		};
	};
```

![coServ workshop #05](https://googledrive.com/host/0B4fEFbbW93y5Y0tsMm1HV2JjSlU)

目前 css 程式碼 3000 多行，有連結顏色的部分多達近90個，今天客戶忽然說要將主要顏色改為某特定色.. 難道只 能 一 個 一 個 改?!

如果是利用 JASS / SASS 只要修改`變數值`就可以了！

* WorkTime
	* 利用 JASS 擴充特性做出兩顆按鈕載入不同樣式

```css
<!--函式-->
<%
	var btn = {
		width: '300px',
		padding: '5px 10px',
		background: '#ff0000',
		'text-align': 'center',
		color:'#fff',
		cursor: 'pointer',
		margin: '5px 0px',
		display: 'block'
	},
	mobile = {
		background: '#00ff00'
	};
	tablet = {
		background: '#0000ff'
	};
%>

.Botton{
	<%=jass.p(btn)%>;
}

<!--擴充-->
.btn_Mobile{
	<%=jass.p(btn)%>;
	<%=jass.p(mobile)%>;
}
.btn_Tablet{
	<%=jass.p(btn)%>;
	<%=jass.p(tablet)%>;
}
```

---

# 2、coServ RWD
[講者投影片 Yoga](http://www.slideshare.net/sh932111/co-serv-rwd)
## 目前主流作法

```scss
@media only screen and(max-width:768px){
	/* 螢幕寬度768載入 */
}
@media only screen and(max-width:600px){
	/* 螢幕寬度600載入 */
}
@media only screen and(max-width:480px){
	/* 螢幕寬度480載入 */
}
```

## coServ 作法簡介3種：

### 1、在 `www/sites.json` 中設定樣板與相對應資料夾 server 將你幫你自動載入是性化的樣板。

```json
"theme": {
            "desktop": "desktop_theme",
            "tablet": "table_theme",
            "mobile": "mobile_theme"
         }
```

### 2、在頁面資料夾加入 JavaScript 檔案內容如下：

```js
ctrl.startup = function(){
	var bi = '<%=JSON.stringify(bi)%>'
	var bi_json = JSON.parse(bi);

	console.log(bi_json);

	console.log('bi.client.category = ' + bi_json.client.category);
	
}
```

結果：

![Chrome Console](https://googledrive.com/host/0B4fEFbbW93y5QmJaenh1WXFiNms)

### 3、在 HTML 頁面判斷

使用 Node.js 語法判斷 `bi.client.category` 來顯示不同文字。

``` html
<h2>Hello World!</h2>

<% if (bi.client.category === 'mobile') { %>
	<h2 class="btn_Mobile">This is mobile</h2>
<% } else if (bi.client.category === 'tablet') { %>
    <h2 class="btn_Tablet">This is tablet</h2>
<% } else { %>
    <h2 class="Botton">This is desktop</h2>
<% } %>
```
結果圖：

![Node.js 語法判斷 ＋ JASS](https://googledrive.com/host/0B4fEFbbW93y5dDNSYU1IWk9sQ1E)