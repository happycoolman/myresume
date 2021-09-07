<template>
  <div class="home">
    <el-carousel :height="style+ 'px'" trigger="click" direction="vertical" :autoplay="false" arrow="always" @change="changeCarousel">
      <!-- 第一页 -->
    <el-carousel-item class="item1">
      <div class="overview">
        <div class="content">
          <div class="info">
          <div class="photo">
            <img src="../assets/me3.jpg" alt="">
          </div>
          <ul class="-list">
            <li class="-item">大专</li>
            <li class="-item">25岁</li>
            <li class="-item">广州</li>
            <li class="-item">已离职</li>
          </ul>
          </div>
          <div class="des">
          <p class="quote">
            生活是一种绵延不绝的渴望，渴望不断上升，变得更好更强。
          </p>
          <div class="des-list">
          <p>我叫刘开幸，通过自学，努力想成为一名前端开发工程师</p>
          <p>1536863186@qq.com</p>
          <p>微信：c85657878</p>
        </div>
          </div>
        </div>
        <i class="jiantou"></i>
      </div>
    </el-carousel-item>
    <el-carousel-item>
      <h2 class="skilltitle">
         能力
      </h2>
       <div class="skill-content">
         <!-- 转圈 -->
         <div class="skill-circle">
           <ul class="out">
            <li class="item" :style="{'backgroundColor': 'rgba(121, 100, 102, 0.8)'}"><span>vue</span></li>
            <li class="item" :style="{'backgroundColor': 'rgba(49, 65, 82, 0.8)'}"><span>js</span></li>
            <li class="item" :style="{'backgroundColor': 'rgba(76, 157, 160, 0.8)'}"><span>html</span></li>
            <li class="item" :style="{'backgroundColor': 'rgba(66, 66, 66, 0.8)'}"><span>css</span></li>
            <li class="item" :style="{'backgroundColor': 'rgba(193, 131, 106, 0.8)'}"><span>node</span></li>
            <li class="item" :style="{'backgroundColor': 'rgba(117, 148, 179, 0.8)'}"><span>web</span></li>
        </ul>
         </div>
         <!-- 右边文字 -->
         <div class="text">
           <p :class="classNamea">自学前端开发</p>
           <p  :class="classNameb">熟悉js高级语法，熟悉vue框架</p>
           <p  :class="classNamec">前后端分离均有尝试，擅长组件开发及构建</p>
           <p  :class="classNamed">自学能力强，抗压能力强</p>
         </div>
      </div>
      <i class="jiantou"></i>
    </el-carousel-item>
    <el-carousel-item>
      <h2 class="skilltitle">
         项目经历
      </h2>
      <div class="content-item3" :class="className">
        <el-carousel indicator-position="outside" height="540px"
        :autoplay="false">
    <el-carousel-item>
      <div class="project1">
        <h6>vue-elementui-admin</h6>
        <p>基于vue+elementui的后台管理项目<br><br>使用Vue-cli 搭建项目,
通过Fastmock构建后台接口JSON数据；封装axios请求后台接口数据渲染页面；
使用Echart让数据可视化<br>
使用less预处理语言，让css更易维护；
</p>
        <img src="../assets/logo.png" alt="">
      </div>
    </el-carousel-item>
    <el-carousel-item>
      <div class="project1">
        <h6>电商后台管理系统</h6>
        <p>
          基于vue+elementui的后台管理项目<br><br>
          使用 模块化开发 商品管理、用户管理、权限管理、修改商品等多个模块。使用 Vue全家桶+ES6语法+less预处理语言等前端技术。
</p>
        <img src="../assets/logo.png" alt="">
      </div>
    </el-carousel-item>
  </el-carousel>
      </div>
      <i class="jiantou"></i>
    </el-carousel-item>
    <el-carousel-item>
        <h2 class="skilltitle">
         工作经历
      </h2>
      <div class="exper" id="avatar">
        <div class="left">
          <img src="../assets/logo.png" alt="">
          <p>佛山维可客电子商务有限公司</p>
        </div>
        <div class="right">
          <p class="title">2020.1 - 2021.5</p>
          <ul>
            <li>产品图片精修</li>
            <li>首页、详情页面设计</li>
            <li>产品包装设计</li>
          </ul>
        </div>
      </div>
      <i class="jiantou"></i>
    </el-carousel-item>
  </el-carousel>
  </div>
</template>

<script>
export default {
  data () {
    return {
      style: '1080',
      classNamea: '',
      classNameb: '',
      classNamec: '',
      classNamed: '',
      className: ''
      // pic: ""
    }
  },
  methods: {
    changeCarousel (e) {
      this.classNamea = ''
      this.classNameb = ''
      this.classNamec = ''
      this.classNamed = ''
      this.className = ''
      if (e === 1) {
        this.classNamea = 'text-item1'
        this.classNameb = 'text-item2'
        this.classNamec = 'text-item3'
        this.classNamed = 'text-item4'
      }
      if (e === 2) {
        this.className = 'caropcity'
      }
    }
  }
}
</script>
