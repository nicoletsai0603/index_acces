# index_acces
banner無障礙

Carousel說明
https://hackmd.io/@VinceChen/BJBZPtg_H

https://www.cnblogs.com/bfc0517/p/6942786.html

<div id="cnblogs_post_body" class="blogpost-body blogpost-body-html">
<p id="head14"><strong>Bootstrap中轮播图插件叫作Carousel，为了清晰的表明每个标签在这里是什么意思，我把解释写在了下面的代码中。</strong></p>
<div class="cnblogs_code"><div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div>
<pre><span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> 
  以下容器就是整个轮播图组件的整体，
  注意该盒子必须加上 class="carousel slide" data-ride="carousel" 表示当前是一个轮播图
  bootstrap.js会自动为当前元素添加图片轮播的特效
</span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
<span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">div </span><span style="color: rgba(255, 0, 0, 1)">id</span><span style="color: rgba(0, 0, 255, 1)">="轮播图的ID"</span><span style="color: rgba(255, 0, 0, 1)"> class</span><span style="color: rgba(0, 0, 255, 1)">="carousel slide"</span><span style="color: rgba(255, 0, 0, 1)"> data-ride</span><span style="color: rgba(0, 0, 255, 1)">="carousel"</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
  <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> ol标签是图片轮播的控制点 </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
  <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">ol </span><span style="color: rgba(255, 0, 0, 1)">class</span><span style="color: rgba(0, 0, 255, 1)">="carousel-indicators"</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
    <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> 
      每一个li就是一个单独的控制点
        data-target属性就是指定当前控制点控制的是哪一个轮播图，其目的是如果界面上有多个轮播图，便于区分到底控制哪一个
        data-slide-to属性是指当前的li元素绑定的是第几个轮播项
      注意，默认必须给其中某个li加上active，展示的时候就是焦点项目
    </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
    <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">li </span><span style="color: rgba(255, 0, 0, 1)">data-target</span><span style="color: rgba(0, 0, 255, 1)">="#轮播图的ID"</span><span style="color: rgba(255, 0, 0, 1)"> data-slide-to</span><span style="color: rgba(0, 0, 255, 1)">="0"</span><span style="color: rgba(255, 0, 0, 1)"> class</span><span style="color: rgba(0, 0, 255, 1)">="active"</span><span style="color: rgba(0, 0, 255, 1)">&gt;&lt;/</span><span style="color: rgba(128, 0, 0, 1)">li</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
    <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">li </span><span style="color: rgba(255, 0, 0, 1)">data-target</span><span style="color: rgba(0, 0, 255, 1)">="#轮播图的ID"</span><span style="color: rgba(255, 0, 0, 1)"> data-slide-to</span><span style="color: rgba(0, 0, 255, 1)">="1"</span><span style="color: rgba(0, 0, 255, 1)">&gt;&lt;/</span><span style="color: rgba(128, 0, 0, 1)">li</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
    <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> ...更多的 </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
  <span style="color: rgba(0, 0, 255, 1)">&lt;/</span><span style="color: rgba(128, 0, 0, 1)">ol</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
  <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> 
    .carousel-inner是所有轮播项的容器盒子，
    注意role="listbox"代表当前div是一个列表盒子，作用就是给当前div添加一个语义
  </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
  <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">div </span><span style="color: rgba(255, 0, 0, 1)">class</span><span style="color: rgba(0, 0, 255, 1)">="carousel-inner"</span><span style="color: rgba(255, 0, 0, 1)"> role</span><span style="color: rgba(0, 0, 255, 1)">="listbox"</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
    <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> 每一个.item就是单个轮播项目，注意默认要给第一个轮播项目加上active，表示为焦点 </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
    <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">div </span><span style="color: rgba(255, 0, 0, 1)">class</span><span style="color: rgba(0, 0, 255, 1)">="item active"</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
      <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> 轮播项目中展示的图片 </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
      <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">img </span><span style="color: rgba(255, 0, 0, 1)">src</span><span style="color: rgba(0, 0, 255, 1)">="example.jpg"</span><span style="color: rgba(255, 0, 0, 1)"> alt</span><span style="color: rgba(0, 0, 255, 1)">="示例图片"</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
      <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">div </span><span style="color: rgba(255, 0, 0, 1)">class</span><span style="color: rgba(0, 0, 255, 1)">="carousel-caption"</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
        <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> 标题或说明性文字，如果不需要，直接删除当前div.carousel-caption </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
      <span style="color: rgba(0, 0, 255, 1)">&lt;/</span><span style="color: rgba(128, 0, 0, 1)">div</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
    <span style="color: rgba(0, 0, 255, 1)">&lt;/</span><span style="color: rgba(128, 0, 0, 1)">div</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
    <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">div </span><span style="color: rgba(255, 0, 0, 1)">class</span><span style="color: rgba(0, 0, 255, 1)">="item"</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
      <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> ... </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
    <span style="color: rgba(0, 0, 255, 1)">&lt;/</span><span style="color: rgba(128, 0, 0, 1)">div</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
    <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> ... </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
  <span style="color: rgba(0, 0, 255, 1)">&lt;/</span><span style="color: rgba(128, 0, 0, 1)">div</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
  <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> 图片轮播上左右两个控制按钮，分别点击可以滚动到上一张和下一张 </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
  <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> 此处需要注意的是 该a链接的href属性必须指向需要控制的轮播图ID </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
  <span style="color: rgba(0, 128, 0, 1)">&lt;!--</span><span style="color: rgba(0, 128, 0, 1)"> 另外a链接中的data-slide="prev"代表点击该链接会滚到上一张，如果设置为next的话则相反 </span><span style="color: rgba(0, 128, 0, 1)">--&gt;</span>
  <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">a </span><span style="color: rgba(255, 0, 0, 1)">class</span><span style="color: rgba(0, 0, 255, 1)">="left carousel-control"</span><span style="color: rgba(255, 0, 0, 1)"> href</span><span style="color: rgba(0, 0, 255, 1)">="#轮播图的ID"</span><span style="color: rgba(255, 0, 0, 1)"> role</span><span style="color: rgba(0, 0, 255, 1)">="button"</span><span style="color: rgba(255, 0, 0, 1)"> data-slide</span><span style="color: rgba(0, 0, 255, 1)">="prev"</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
    <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">span </span><span style="color: rgba(255, 0, 0, 1)">class</span><span style="color: rgba(0, 0, 255, 1)">="glyphicon glyphicon-chevron-left"</span><span style="color: rgba(255, 0, 0, 1)"> aria-hidden</span><span style="color: rgba(0, 0, 255, 1)">="true"</span><span style="color: rgba(0, 0, 255, 1)">&gt;&lt;/</span><span style="color: rgba(128, 0, 0, 1)">span</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
    <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">span </span><span style="color: rgba(255, 0, 0, 1)">class</span><span style="color: rgba(0, 0, 255, 1)">="sr-only"</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>上一张<span style="color: rgba(0, 0, 255, 1)">&lt;/</span><span style="color: rgba(128, 0, 0, 1)">span</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
  <span style="color: rgba(0, 0, 255, 1)">&lt;/</span><span style="color: rgba(128, 0, 0, 1)">a</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
  <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">a </span><span style="color: rgba(255, 0, 0, 1)">class</span><span style="color: rgba(0, 0, 255, 1)">="right carousel-control"</span><span style="color: rgba(255, 0, 0, 1)"> href</span><span style="color: rgba(0, 0, 255, 1)">="#轮播图的ID"</span><span style="color: rgba(255, 0, 0, 1)"> role</span><span style="color: rgba(0, 0, 255, 1)">="button"</span><span style="color: rgba(255, 0, 0, 1)"> data-slide</span><span style="color: rgba(0, 0, 255, 1)">="next"</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
    <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">span </span><span style="color: rgba(255, 0, 0, 1)">class</span><span style="color: rgba(0, 0, 255, 1)">="glyphicon glyphicon-chevron-right"</span><span style="color: rgba(255, 0, 0, 1)"> aria-hidden</span><span style="color: rgba(0, 0, 255, 1)">="true"</span><span style="color: rgba(0, 0, 255, 1)">&gt;&lt;/</span><span style="color: rgba(128, 0, 0, 1)">span</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
    <span style="color: rgba(0, 0, 255, 1)">&lt;</span><span style="color: rgba(128, 0, 0, 1)">span </span><span style="color: rgba(255, 0, 0, 1)">class</span><span style="color: rgba(0, 0, 255, 1)">="sr-only"</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>下一张<span style="color: rgba(0, 0, 255, 1)">&lt;/</span><span style="color: rgba(128, 0, 0, 1)">span</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
  <span style="color: rgba(0, 0, 255, 1)">&lt;/</span><span style="color: rgba(128, 0, 0, 1)">a</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span>
<span style="color: rgba(0, 0, 255, 1)">&lt;/</span><span style="color: rgba(128, 0, 0, 1)">div</span><span style="color: rgba(0, 0, 255, 1)">&gt;</span></pre>
<div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div></div>
<p>可以和源码对比看一下，源码地址：<a href="http://v3.bootcss.com/javascript/#carousel" target="_blank" rel="noopener">http://v3.bootcss.com/javascript/#carousel</a></p>
</div>
