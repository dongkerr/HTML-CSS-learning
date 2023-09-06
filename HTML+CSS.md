# HTML + CSS

## 前端工程师的职责

* 无论是前端还是后台工程师我们的工作都是开发软件

* 现在的主流软件都是C/S架构，C即客户端，S即服务器

  * 用户通过客户端来使用软件
  * 服务器为用户提供各种服务器

* 客户端的呈现形式

  1. 传统的图形化界面的客户端

     * office、qq、360安全卫士、王者荣耀、和平精英...
     * 特点：
       * 需要安装，跨平台性差！
       * 开发成本高

  2. 以网页为界面（interface）的客户端（B/S架构）

     * 京东、淘宝、知乎....

     * 特点：
       * 不需要安装，跨平台性好！
       * 开发成本低

* 前端工程师就是负责写网页的

## 网页的概述

* 万维网的发明者是添·伯纳斯·李
* 网页需要运行到浏览器中，有些企业嗅到商机开始着手制作浏览器
* 网景公司、微软公司，当时比较大的浏览器厂商
* 生产浏览器的公司，为了竞争市场份额开始了第一次浏览器大战，最终微软IE浏览器取得了胜利
* 由于浏览器之间的恶性竞争，引发了网页的兼容问题，同样一个网页在不同的浏览器中显示效果不同
* 为了解决这个问题，伯纳斯李创建了W3C（万维网联盟）专门负责指定万维网中的各种标准
* 由于在第二次浏览器大战中，Google公司的Chrome取得绝对的胜利，所以现在开发中几乎不再需要考虑兼容性问题了
* 根据W3C的规范，一个网页被分成了三个部分：
  * 结构、表现、行为
    * 结构，网页的结构，网页中哪里是标题、哪里是图片、哪里是链接
      * html负责定义网页的结构
    * 表现，网页的外在样式，网页的颜色，网页的布局...
      * css负责网页的表现
    * 行为，网页和用户的交互行为
      * JavaScript负责网页的行为
  * 文档：
    * https://developer.mozilla.org/zh-CN/
  * 简历：
    * 熟悉W3C的网页规范，能开发符合W3C标准的页面

## HTML

* HTML负责网页的结构
* Hyper Text Markup Language（超文本标记语言）
  * 文本：在计算机中使用纯文本编辑器编写的内容被称为文本
    * word编写的内容不是纯文本，而是富文本
  * 网页的扩展名为.html，一个网页最终由浏览器渲染呈现
  * 标记：标记用来告诉浏览器中，网页中的不同内容
    * 在网页中使用html标签作为标记，来标记出不同的内容
    * html标签：
      * 成对出现：
      * <标签名></标签名>

* HTML就是通过不同的标签来标识出网页中的不同内容，学习HTML就是学习各种标签

* 在实际开发中，不推荐用记事本去编写代码，可以使用一些其他的纯文本编辑器来编写代码（nodepad++）

  * 更多的是用IDE（vscode、webstorm）

* 网页的基本结构：

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
  </head>
  <body>
      
  </body>
  </html>
  ```

* !DOCTYPE html
  * 文档生命，用来声明网页的版本，这个用来标识当前网页是遵循HTML5规范的
  * doc指document，表示文档，文档就是网页，一个网页就是一个文档
  * type指类型
* html
  * html根标签，一个网页有且只有一个根标签，其他标签都应该在根标签内部
* head
  * html的子标签（子元素）
  * head表示网页的头部，可以在head中设置网页的各种数据，head中的内容不会在网页中直接显示
  * meta
    * head的子元素，用来设置网页的元数据
    * charset="UTF-8"（属性名=属性值），主要用来避免乱码问题
  * title
    * head的子元素，用来设置网页的标题，会显示在标签上
* body
  * html的子标签（子元素）
  * 网页中所有可见的内容都应该写在body的里面

## html的语法

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML的语法</title>
</head>
<body>
    <!--
        注释，注释中的内容不会在网页中显示，只会显示在源码中
        通过主食可以对代码进行解释说明，也可以隐藏界面中一些不希望显示的内容
        作为一个程序员，要养成良好的编写注释的习惯，注释要求简单明了

        注释不能进行嵌套！
    -->
    <!-- 这是重要的内容不要删 -->
    
    <h1>HTML的语法</h1>

    <!-- 
        HTML的基本语法
            标签；
                一个标签，也被称为是一个标签
                成对出现:<标签名>标签体</标签名>
                自结束标签：<标签名>
                自结束标签：<标签名 />
            
            属性：
                在开始标签中（或自结束标签）中可以为元素设置属性，
                  属性用来描述元素，属性是一个名值对结构，属性名="属性值"
                  一个元素可以同时指定多个属性，多个属性之间使用空格分离
                
                有些属性，属性名和属性值相同，此时可以省略属性值
            
            html中不区分大小写，但是建议用小写
     -->        
     
    
    <input type="text" name="username">
    <br>
    <input type="radio" checked>
    <br />
    今天天气真不错！
    
</body>
</html>
```

## 元素间的关系

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>元素间的关系</title>
</head>
<body>
    <!-- 
        标签tag
        元素element

        元素之间的关系：
            父元素
                - 直接包含子元素的元素是父元素
            子元素
                - 直接被父元素包含的元素
            祖先元素
                - 直接或间接包含后代元素的元素是祖先元素
                - 父元素也是祖先元素
            后代元素
                - 直接或间接被祖先元素包含的元素是后代元素
                - 子元素也是后代元素
            兄弟元素
                - 拥有相同的父元素的元素是兄弟元素

     -->
    
</body>
</html>
```

## 常用的标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- 
        title表示标题标签，文字会显示到标签页上，
        搜索引擎在抓去页面中，会通过title的内通来识别网页的主要内容
        这部分主要是SEO相关的知识（SEO搜索引擎优化）
     -->
    <title>常用标签</title>
</head>
<body>
    <!-- 
        标题标签
            一共有6级标题，从h1-h6
            h1最大，h6最小，从语义上讲，h1最重要，h2其次，h3再次..
            注意：对于html标签来说，我们关注的是标签语义，而不是它的样式

            在SEO中h1的重要性仅次于title，搜索引擎也会通过h1来识别页面的主要信息
                通常一个页面只有一个h1

     -->
    <h1>一级标题</h1>
    <h2>二级标题</h2>
    <h3>三级标题</h3>
    <h4>四级标题</h4>
    <h5>五级标题</h5>
    <h6>六级标题</h6>
    

     <!-- 
        p 标签标识一个段落
      -->
    <p>我是一个段落</p>
    

    <!-- 
        br 表示换行
     -->
    <br>

    <!-- 
        hr 表示水平线
     -->
    <hr>
    

    <!-- 
        可以通过实体在网页中来表示一些特殊符号
            语法：&实体的名字；
            常用：
                &lt; 小于号
                &gt; 大于号
                &nbsp; 空格
                &copy; 版权符号
     -->
    a&lt;b>c
    a&lt;b&gt;c

    <br>

    <!-- 
        在html中会忽略多个空格和换行，
        多个空格和换行会被识别为一个空格
     -->

     &copy;李明昊真&nbsp;&nbsp;&nbsp;帅！
    <br>
    aaaaaaaaaaaaaa &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;bbbbbb


</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 
        标签列表：
            https://developer.mozilla.org/en-US/docs/Web/HTML/Element
        列表
            有序列表
                - 使用ol来创建有序列表
                - 在ol中使用li来表示列表项
            无序列表
                - 用ul来创建无序列表
                - 在ul中使用li来表示列表项
            定义列表
                - 定义列表用来描述一些内容
                - 使用dl来创建定义列表
                - 使用dt来定义被描述的内容
                - 使用dd来对内容进行描述


            1. 芹菜
            2. 萝卜
            3. 大闸蟹
     -->
    
    <ol>
        <li>芹菜</li>
        <li>萝卜</li>
        <li>大闸蟹</li>
    </ol>
    <ul>
        <li>芹菜</li>
        <li>萝卜</li>
        <li>大闸蟹</li>
    </ul>

<!-- 列表之间可以互相嵌套-->

<ul>
    <li>
        鱼香肉丝
        <ol>
            <li>鱼</li>
            <li>香</li>
            <li>肉丝</li>
        </ol>
    </li>
    <li>宫保鸡丁</li>
    <li>西红柿炒番茄</li>
</ul>

<dl>
    <dt>李明昊</dt>
    <dd>瑞士知名歌舞伎</dd>
    <dt>大闸蟹</dt>
    <dd>宁波著名大螃蟹</dd>
    <dd>以擅长横着走路著称</dd>
</dl>

</body>
</html>
```

## 语义化标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>语义化标签</title>
</head>
<body>
    <!-- 
        网页除了需要被人看，还需要爬虫程序爬取，
          w3c就希望能够帮助程序更好地爬取这个页面
          于是他就添加了很多不同的语义化标签来帮助程序来识别页面
          

          main 主要内容，一个页面中最好只有一个main标签
          header 头部内容
          footer 底部内容
          article 表示独立的内容
          aside 侧边栏，和主体独立的内容
          nav 表示导航
          section 独立的区块
          em 斜体加强
             Marks text that has stress emphasis. 
             The <em> element can be nested, with each nesting level indicating a greater degree of emphasis.
          cite 用于包含引用作品的标题。这个引用可能是一个根据适当的上下文约定关联引用的元数据的缩写。
          s 使用删除线来渲染文本。
          img 将一张图像嵌入文档。
          area 在图片上定义一个可点击区域。图像映射（image map）允许图像上的几何区域与超链接关联。
          var 表示数学表达式或编程上下文中的变量名称。尽管该行为取决于浏览器，但通常使用当前字体的斜体形式显示。


          通过这些语义化标签，可以对网页中的不同内通进行描述，
            方便爬虫程序识别页面，但是大部分情况下我们不会大量使用这些标签
        
          实际开发中，比较常见的是，使用div代替所有标签


          作业1:
            分别为上述7个标签创建一个demo
          作业2:
            查看mdn文档，找到5个标签，并注明他们的作用
          固定作业：
            整理笔记
     -->
    <header>头部内容</header>
    <main>主题内容</main>
    <footer>底部内容</footer>
    <article class="forcast">
        <h1>Weather forcast for <em>Zürich</em></h1>
        <article class="day-forcast">
            <h2>07 September 2023</h2>
            <p><s>Rain.</s>Rain.</p>
        </article>
        <article class="day-forcast">
            <h2>08 September 2023</h2>
            <p>Periods of rain.</p>
        </article>
        <article class="day-forcast">
            <h2>09 September 2023</h2>
            <p>Heavy rain.</p>
        </article>
    </article>
    <aside>
        <p>how will the weather be</p>
    </aside>
    <nav class="crumbs">
        <ol>
          <li class="crumb"><a href="#">Bikes</a></li>
          <li class="crumb"><a href="#">BMX</a></li>
          <li class="crumb">Jump Bike 3000</li>
        </ol>
      </nav>
      <section>
        <h2>Introduction</h2>
        <p><cite>This document</cite> provides a guide to help with the important task of choosing the correct Apple.</p>
      </section>
</body>
</html>
```

