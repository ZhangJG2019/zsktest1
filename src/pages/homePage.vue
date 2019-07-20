<template>
  <div class="home-page container">
    <main style="background:#F2F2F2;    padding-bottom: 80px">
      <!-- logo and searchbox 1-->
      <div class="header">
        <div class="row">
          <div class="index-contents col-sm-4">
            <img src="../assets/logo2.png" alt="" />
          </div>
          <div class="index-contents col-sm-7" style="float:left;margin:14px 0">
            <el-input
              placeholder="请输入内容"
              v-model="input3"
              class="input-with-select"
            >
              <el-select v-model="select" slot="prepend" placeholder="请选择">
                <el-option label="餐厅名" value="1"></el-option>
                <el-option label="订单号" value="2"></el-option>
                <el-option label="用户电话" value="3"></el-option>
              </el-select>
              <el-button slot="append" icon="el-icon-search"></el-button>
            </el-input>
          </div>
        </div>
      </div>
      <!-- logo and searchbox 2-->
      <!-- 中间所有内容 1-->
      <div class="containers">
        <div class="row">
          <!-- 左侧内容 -->
          <div class="index-content col-md-3 col-sm-4">
            <div class="side_left">
              <!-- 最新事件 -->
              <div class=" news mb15">
                <h2>
                  <a href=""><strong>最新事件</strong></a>
                </h2>
                <ul class="left_ul left_content">
                  <!--<li v-for="(item, key) in topNews" :key="key"> 
                            <span>{{date | formatDate}}</span>
                            <a href="" v-text="n.title"></a> 
                        </li> -->
                  <li>
                    <span>{{ date | formatDate1 }}</span
                    ><a href="####">社会主义接班人团结友善敬业</a>
                  </li>
                  <li>
                    <span>{{ date | formatDate1 }}</span
                    ><a href="####">社会主义接班人团结友善敬业</a>
                  </li>
                  <li>
                    <span>{{ date | formatDate1 }}</span
                    ><a href="####">社会主义接班人团结友善敬业</a>
                  </li>
                  <li>
                    <span>{{ date | formatDate1 }}</span
                    ><a href="####">社会主义接班人团结友善敬业</a>
                  </li>
                  <li>
                    <span>{{ date | formatDate1 }}</span
                    ><a href="####">社会主义接班人团结友善敬业</a>
                  </li>
                  <li>
                    <span>{{ date | formatDate1 }}</span
                    ><a href="####">社会主义接班人团结友善敬业</a>
                  </li>
                  <li>
                    <span>{{ date | formatDate1 }}</span
                    ><a href="####">社会主义接班人团结友善敬业</a>
                  </li>
                  <li>
                    <span>{{ date | formatDate1 }}</span
                    ><a href="####">社会主义接班人团结友善敬业</a>
                  </li>
                  <!-- <li v-for="(item, key) in itemlis" :key="key">
                            {{ item.title }}
                        </li> -->
                </ul>
              </div>
              <!-- 最新研究内容 -->
              <div class=" news">
                <h2>
                  <a href=""><strong>最新研究内容</strong></a>
                </h2>
                <ul id="newlog" class="left_content">
                  <!-- <li class="odd"> <div v-text="n.id" class="new_content "></div><a href="" v-text="n.title"></a> </li> -->
                  <li>
                    <div class="new_content ">1</div>
                    <a href=""
                      >富强民主文明和谐自由平等公正法治爱国敬业诚信友善</a
                    >
                  </li>
                  <li>
                    <div class="new_content ">2</div>
                    <a href=""
                      >富强民主文明和谐自由平等公正法治爱国敬业诚信友善</a
                    >
                  </li>
                  <li>
                    <div class="new_content ">3</div>
                    <a href=""
                      >富强民主文明和谐自由平等公正法治爱国敬业诚信友善</a
                    >
                  </li>
                  <li>
                    <div class="new_content ">4</div>
                    <a href=""
                      >富强民主文明和谐自由平等公正法治爱国敬业诚信友善</a
                    >
                  </li>
                  <li>
                    <div class="new_content ">5</div>
                    <a href=""
                      >富强民主文明和谐自由平等公正法治爱国敬业诚信友善</a
                    >
                  </li>
                  <li>
                    <div class="new_content ">6</div>
                    <a href=""
                      >富强民主文明和谐自由平等公正法治爱国敬业诚信友善</a
                    >
                  </li>
                  <li>
                    <div class="new_content ">7</div>
                    <a href=""
                      >富强民主文明和谐自由平等公正法治爱国敬业诚信友善</a
                    >
                  </li>
                  <li>
                    <div class="new_content ">8</div>
                    <a href=""
                      >富强民主文明和谐自由平等公正法治爱国敬业诚信友善</a
                    >
                  </li>
                  <li>
                    <div class="new_content ">9</div>
                    <a href=""
                      >富强民主文明和谐自由平等公正法治爱国敬业诚信友善</a
                    >
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <!-- 中间内容 -->
          <div class="index-content col-md-6 col-sm-5">
            <div class="slide_center fl">
              <div class=" news bgc_white">
                <h2>
                  <a href="####"><strong>分类标签</strong></a>
                </h2>
                <ul>
                  <!-- <li v-for="n in topNews" class="center_content"> -->
                  <!-- <i class=""></i>
							<a href="####" v-text="n.title" class="title"></a><br>
							<a href="####" v-text="n.id" class="num"></a> -->
                  <li class="center_content">
                    <img src="../assets/images/content/jiyin.png" alt="" />
                    <a href="####" class="title">基因</a><br />
                    <a href="####" class="num">123</a>
                  </li>
                  <li class="center_content">
                    <img
                      src="../assets/images/content/xianguanyaowu.png"
                      alt=""
                    />
                    <a href="####" class="title">药物</a><br />
                    <a href="####" class="num">456</a>
                  </li>
                  <li class="center_content">
                    <img
                      src="../assets/images/content/yaowujiyindui.png"
                      alt=""
                    />
                    <a href="####" class="title">药物基因对</a><br />
                    <a href="####" class="num">789</a>
                  </li>
                  <li class="center_content">
                    <img
                      src="../assets/images/content/quanweizhinan.png"
                      alt=""
                    />
                    <a href="####" class="title">权威指南</a><br />
                    <a href="####" class="num">987</a>
                  </li>
                  <li class="center_content">
                    <img
                      src="../assets/images/content/yaowubiaoqian.png"
                      alt=""
                    />
                    <a href="####" class="title">药物标签</a><br />
                    <a href="####" class="num">654</a>
                  </li>
                  <li class="center_content">
                    <img
                      src="../assets/images/content/linchuangzhushi.png"
                      alt=""
                    />
                    <a href="####" class="title">临床注释</a><br />
                    <a href="####" class="num">321</a>
                  </li>
                  <li class="center_content">
                    <img
                      src="../assets/images/content/linchuangshiyan.png"
                      alt=""
                      style="width:100px;height:80px"
                    />
                    <a href="####" class="title">临床实验</a><br />
                    <a href="####" class="num">1314</a>
                  </li>
                  <li class="center_content">
                    <img src="../assets/images/content/zhuanli.png" alt="" />
                    <a href="####" class="title">专利</a><br />
                    <a href="####" class="num">521</a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <!-- 右侧内容 -->
          <div class="side_left fl index-content col-md-3 col-sm-3">
            <!-- 公告 -->
            <div class=" news">
              <h2>
                <a href=""><strong>公告</strong></a>
              </h2>
              <ul class="right_contents">
                <li><span>1</span> <a>更新说明</a></li>
                <li><span>2</span> <a>浏览数据量</a></li>
                <li><span>3</span> <a>导出数据量</a></li>
                <li><span>4</span> <a>版本更新</a></li>
                <li><span>5</span> <a>用户量/词条量</a></li>
                <!-- <li v-for="n in topNews" class="odd"><a href="" v-text="n.title"></a></li> -->
              </ul>
            </div>
            <!-- 联系 -->
            <div class=" news tel h535  mt20">
              <h2 class="">
                <a href="####"><strong>联系</strong></a>
              </h2>
              <div class="phone content">
                <!-- <i class="iconfont icon-dianhua-1"></i> -->
                <a href="####" class="phone_ul"></a>
              </div>
              <div class="email content">
                <!-- <i class="iconfont icon-huaban-"></i> -->
                <a href="####" class="email_ul"></a>
              </div>
              <!-- 我要留言 1-->
              <div class="Message mt22 h276">
                <h2 class="leaveMessage">我要留言</h2>
              </div>
            </div>
            <!-- 右下留言input 1-->
            <div class="right_bottom"></div>
            <!-- 右下留言input 2-->
          </div>
          <!-- 业务划分区域 start -->
          <div class="header_bottom">
            <div class="index-content  col-md-3 guide_ul">
              <a href="####">
                <i class="iconfont icon-yonghuguanli"></i>
                <p>知识库用户</p>
              </a>
            </div>
            <div class="index-content  col-md-3 guide_ul">
              <a href="####">
                <i class="iconfont icon-xiazai-xianxing"></i>
                <p>下载</p>
              </a>
            </div>
            <div class="index-content  col-md-3 guide_ul">
              <a href="####">
                <i class="iconfont icon-icon"></i>
                <p>帮助</p>
              </a>
            </div>
            <div class="index-content  col-md-3 guide_ul">
              <a href="taskcontrol.html">
                <i class="iconfont icon-woderenwu"></i>
                <p>任务大厅</p>
              </a>
            </div>
          </div>
          <!-- 业务划分区域 end -->
        </div>
      </div>
      <!-- 中间所有内容 2-->
      <div class="clearfix"></div>
    </main>
  </div>
</template>

<script>
import $ from 'jquery';
import '../assets/css/font2/iconfont.css';
import '../assets/css/font/iconfont.css';

// 事件补位函数 1
var padDate = function(value) {
  return value < 10 ? '0' + value : value;
};
// 事件补位函数 2
// 格式化时间函数 1
var formatDate = function(value) {
  // 这里的value就是需要过滤的数据
  var date = new Date(value);
  var year = date.getFullYear();
  var month = padDate(date.getMonth() + 1);
  var day = padDate(date.getDate());
  return year + '-' + month + '-' + day;
};
// 格式化时间函数 2

export default {
  data() {
    return {
      date: new Date(),
      input1: '',
      input2: '',
      input3: '',
      select: ''
    };
  },
  filters: {
    formatDate1: formatDate // 最新事件的时间处理函数
  },
  mounted() {
    // 中间背景添加 1
    function bgc(color, tagName) {
      $(tagName).each(function(i, e) {
        $(e).css('background-color', color[i]);
      });
    }
    bgc(['orange', 'orange', 'orange'], '#newlog li div');
    bgc(['#35be9b', '#8bc255', '#56bde3', '#f78228'], '.guide_ul ');
    bgc(
      [
        '#fe6181',
        '#5fc46d',
        '#6661d5',
        '#01c4c3',
        '#62b6e5',
        '#ff6765',
        '#7dc691',
        '#feab1c'
      ],
      '.slide_center .news li'
    );
    // 中间背景添加 2
    // 业务划分区域页面跳转 1
    $('guide_ul').click(function() {
      $('a', this)[0].click();
    });
    // 业务划分区域页面跳转 2
  }
};
</script>

<style scoped>
@import '../style/style.css';
@import '../style/base.css';
@import '../style/index.css';
@import '../style/bootstrap-flat.min.css';
.hezuo {
  width: 100%;
}
.right_contents {
  height: 217px;
  border: 1px solid #ddd;
  border-top: 0;
  padding-top: 10px;
  box-sizing: border-box;
  background-color: #fff;
}
.right_contents li {
  width: 100%;
}
.news ul li img {
  width: 80px;
  height: 80px;
  margin: 23px 0 0 66px;
}
.header_bottom {
  margin: 0 15px;
}
.guide_ul {
  height: 76px;
  cursor: pointer;
  border: 1px solid #ccc;
  margin-top: 20px;
}
.guide_ul i {
  font-size: 45px;
  color: white;
  margin: 7px 0 0 15px;
  float: left;
}
.guide_ul p {
  margin-left: 16px;
  height: 76px;
  line-height: 76px;
  font-size: 20px;
  color: #fff;
  float: left;
}
.page-header {
  margin: 0;
}
.searchbox {
  width: 7.7em;
}
.head_bgc {
  float: right;
  background-color: #e8e8e8;
  height: 2.9em;
  line-height: 2.6em;
  border-radius: 5px;
  border: 1px solid #ebebeb !important;
}
.logo {
  float: left;
}
.searchbox {
  float: right;
  width: 100%;
}
/*清除浮动代码*/
.clearflx:after {
  display: block;
  clear: both;
  content: '';
  visibility: hidden;
  height: 0;
}
.clearflx {
  zoom: 1;
}
.no-padding {
  padding-right: 0 !important;
}
.container {
  /* padding-left: 0; */
  box-sizing: border-box;
}
</style>
