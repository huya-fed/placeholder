# placeholder 使用介绍

针对不支持placeholder的浏览器做的模拟支持




##用法

###html

	<p><label><code>type=search</code> <input type="search" name="search" placeholder="Search this site…" class="a"></label></p>
	<p><label><code>type=email</code> <input type="email" name="email" placeholder="e.g. address@example.ext" class="a"></label></p>
	<p><label><code>type=url</code> <input type="url" name="url" placeholder="e.g. http://mathiasbynens.be/" class="a"></label></p>
	<p><label><code>type=tel</code> <input type="tel" name="tel" placeholder="e.g. +32 472 77 69 88" class="a"></label></p>
	<p><label for="p"><code>type=password</code> </label><input type="password" name="password" placeholder="e.g. hunter2" id="p" class="a"></p>
	<p><label><code>textarea</code> <textarea name="message" placeholder="Your message goes here" class="a"></textarea></label></p>

###css

	/*可以通过改变这个class的样式去改变placeholder的样式，插件默认加上placeholder*/
	.placeholder {
			color:#f60;
	}


	::-webkit-input-placeholder { /* WebKit browsers */
    	color:    #909;
	}
	:-moz-placeholder { /* Mozilla Firefox 4 to 18 */
	   color:    #909;
	   opacity:  1;
	}
	::-moz-placeholder { /* Mozilla Firefox 19+ */
	   color:    #909;
	   opacity:  1;
	}
	:-ms-input-placeholder { /* Internet Explorer 10+ */
	   color:    #909;
	}


###js

	var placeholder = require('placeholder');

	placeholder('.a');

	// 提供---提前清除掉 placeholder 带来的 value，提交表单
     placeholder.clear('#test-input-2');