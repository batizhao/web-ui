web-ui
======

## 前端架构要求

* 使用 HTML5，但要保证浏览器兼容。兼容 IE8+，Safari，Chrome，Firefox。
* 主要使用 JQuery。
* 方便的多主题切换（不止皮肤，还包括布局），这部分可能需要结合部分后台程序，但在前端架构上要考虑和支持这一点。
* 尽量少的图片，所有的小图标用 Sprites。
* 注意静态文件的数量，只把必要先加载的 JS 放在头部。
* 重点关注性能，主要关注 HTTP 请求数，加载顺序、脚本阻塞。
* 重复出现的样式，脚本必须放到 css、js 文件中。
* 所有静态文件、代码命名要规范。
* 保持代码干净，无冗余代码。
* 不使用 frame，除非必要的情况。
* 在移动设备（iPad）可以基本正常操作。

## 目录结构规范

    .
    |-- 403.html
    |-- 404.html
    |-- 500.html
    |-- favicon.ico
    |-- favicon.png
    |-- images
        |-- … .png
        |-- … .jpg
    	|-- … .gif
    |-- scripts
        |-- jquery-1.8.0.js
        |-- … .js
    |-- index.html
    |-- … .html
    |-- styles
        |-- base.css
        |-- ...            
        |-- theme1
        	|-- images
        		|-- … .png
        		|-- … .jpg
    			|-- … .gif
        	|-- layout.css
        	|-- theme.css
        |-- theme2
        	|-- images
        		|-- ...
        	|-- layout.css
        	|-- theme.css
        |-- theme3
        	|-- images
        		|-- ...
        	|-- layout.css
        	|-- theme.css


- **images**  
	基础图片目录。

- **scripts**  
	脚本目录。

- **styles**   
    基础样式文件。

- **theme**  
	主题相关样式、图片，默认 theme1。具体 theme 的名字根据实际情况修改。

## 前后端交互

* 主要采用 AJAX + JSON 方式。
* 所有页面（主要是查询相关），先展示页面，再加载数据（耗时操作提供进度条）。

## 前端的主要工作

* 建设基础 UI 组件库
* 列表的 AJAX 加载
* 列表的修改、删除（批量删除）操作、交互校验
* 统一的模态交互窗口
* 成功、失败、警告提示
* 表单校验
* 进度条
* 上传组件、客户端文件大小校验
* 自动完成
* API 文档
* 配合后端程序员完成页面相关的功能

## 后端和前端结合部分的工作

* 静态 CSS 和 JS 文件的压缩和合并会在应用程序打包时自动完成，前端不用关心这一点，但必须保证这些文件压缩、合并之后不会出现冲突。
* Gzip、Expires、文件名动态时间戳 这些参数会在服务端配置，前端不用关心。
* 后端程序员完成和业务逻辑相关的编码（表单参数校验、Submit、GET/PUT/POST/DELETE）。

## 推荐参考

* [Twitter Bootstrap](http://twitter.github.com/bootstrap/index.html)
* [Jekyll Bootstrap](http://jekyllbootstrap.com)
* [Wordpress](http://wordpress.org)









