# index_acces
banner無障礙

Carousel說明
https://hackmd.io/@VinceChen/BJBZPtg_H

https://www.cnblogs.com/bfc0517/p/6942786.html

<!-- 
  以下容器就是整个轮播图组件的整体，
  注意该盒子必须加上 class="carousel slide" data-ride="carousel" 表示当前是一个轮播图
  bootstrap.js会自动为当前元素添加图片轮播的特效
-->
<div id="轮播图的ID" class="carousel slide" data-ride="carousel">
  <!-- ol标签是图片轮播的控制点 -->
  <ol class="carousel-indicators">
    <!-- 
      每一个li就是一个单独的控制点
        data-target属性就是指定当前控制点控制的是哪一个轮播图，其目的是如果界面上有多个轮播图，便于区分到底控制哪一个
        data-slide-to属性是指当前的li元素绑定的是第几个轮播项
      注意，默认必须给其中某个li加上active，展示的时候就是焦点项目
    -->
    <li data-target="#轮播图的ID" data-slide-to="0" class="active"></li>
    <li data-target="#轮播图的ID" data-slide-to="1"></li>
    <!-- ...更多的 -->
  </ol>
  <!-- 
    .carousel-inner是所有轮播项的容器盒子，
    注意role="listbox"代表当前div是一个列表盒子，作用就是给当前div添加一个语义
  -->
  <div class="carousel-inner" role="listbox">
    <!-- 每一个.item就是单个轮播项目，注意默认要给第一个轮播项目加上active，表示为焦点 -->
    <div class="item active">
      <!-- 轮播项目中展示的图片 -->
      <img src="example.jpg" alt="示例图片">
      <div class="carousel-caption">
        <!-- 标题或说明性文字，如果不需要，直接删除当前div.carousel-caption -->
      </div>
    </div>
    <div class="item">
      <!-- ... -->
    </div>
    <!-- ... -->
  </div>
  <!-- 图片轮播上左右两个控制按钮，分别点击可以滚动到上一张和下一张 -->
  <!-- 此处需要注意的是 该a链接的href属性必须指向需要控制的轮播图ID -->
  <!-- 另外a链接中的data-slide="prev"代表点击该链接会滚到上一张，如果设置为next的话则相反 -->
  <a class="left carousel-control" href="#轮播图的ID" role="button" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
    <span class="sr-only">上一张</span>
  </a>
  <a class="right carousel-control" href="#轮播图的ID" role="button" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    <span class="sr-only">下一张</span>
  </a>
</div>
