<template>
  <section class="pubCon">
    <div class="pubTit">
      <h2>关于我们</h2>
      <h3>ABOUT US</h3>
    </div>
    <!-- 内容区域 -->
    <div class="aboCon">
      <article class="lt">{{ about_cont }}</article>
      <div class="rt">
        <img src="@/assets/banner.jpg" alt="" />
        <div class="boxLine"></div>
        <!-- <router-link to="/about"><div class="btn fa fa-long-arrow-right"></div></router-link> -->
      </div>
    </div>
    <!-- 分类区域 -->
    <!-- <div class="aboItems">
      <div class="item" v-for="item in itemList" :key="item.id">
        <i class="fa fa-camera-retro fa-2x"></i>
        <span>{{ item.title }}</span>
        <span>{{ item.content }}</span>
      </div> -->
    <!-- </div> -->
  </section>
</template>

<script>
export default {
  data() {
    return {
      about_cont:
        '公司于2016年创办成立，总部位于浙江省杭州市国家高新技术产业开发区，是一家集研发、生产、销售、服务为一体的高新技术企业。公司主营业务：气象仪器、环保仪器以及解决方案。公司为自然资源部、环保部、气象局、民航、科研院所、高校等不同领域用户提供了高性能监测设备、分析仪器、运维服务以及创新产品组合和解决方案。公司先后为多个国家级重大项目提供保障工作，分别参与了2022年北京冬奥会和冬残奥会气象服务保障、2019年第七届世界军人运 动会环境空气质量保障工作、中华人民共和国成立70周年庆祝活动气象服务保障等重大项目，均取得圆满成功，专业水平和服务能力得到用户一致的好评和认可',
      itemList: [
        //导航
        { id: '001', title: '穿衣', content: '穿衣品味是培养你时尚感的一步' },
        { id: '002', title: '化妆', content: '化妆让你拥有更完美的容颜更自信' },
        { id: '003', title: '塑性', content: '系统的塑性训练让你更有气质' },
        { id: '004', title: '穿衣', content: '穿衣品味是培养你时尚感的一步' },
      ],
    };
  },
};
</script>

<style scoped>
.aboCon {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center; /*垂直居中*/
}
.aboCon .lt {
  width: 50%;
  color: #aaaaaa;
  padding: 40px;
  line-height: 25px;
  text-align: justify;
}
.aboCon .rt {
  width: 50%;
  position: relative;
}
.aboCon .rt img {
  width: 100%;
}
.aboCon .rt .boxLine {
  position: absolute;
  width: 70%;
  height: 170px;
  border: 1px solid #b09c70;
  right: -20px;
  bottom: -20px;
  z-index: -1;
}
.aboCon .btn {
  background-color: #b09c70;
  color: #ffffff;
  text-align: center; 
  font-size: 14px;
  position: absolute;
  bottom: 70px;
  left: -62px;
  cursor: pointer;
  padding: 8px 40px;
  transition: 0.2s;
}
.aboCon .btn:hover {
  background-color: #CEB989; 
}
.aboItems {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  margin: 80px 0;
}
.aboItems .item {
  padding: 20px 20px;
  width: 25%;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  -ms-flex-direction: column;
  flex-direction: column;
  text-align: center;
}
.aboItems .item i {
  color: #b09c70;
}
.aboItems .item span:nth-child(2) {
  color: #333333;
  font-weight: bold;
  line-height: 50px;
  display: inline-block;
}

.aboItems .item span:nth-child(3) {
  color: #aaaaaa;
  line-height: 25px;
  display: inline-block;
}

/* 小于768 */
@media (max-width: 768px) {
  .aboCon {
    -webkit-box-orient: vertical;
    -webkit-box-direction: reverse;
    -ms-flex-direction: column-reverse;
    flex-direction: column-reverse;
  }
  .aboCon .lt {
    width: 90%;
    padding: 0px;
  }
  .aboCon .rt {
    padding-top: 20px;
    padding-bottom: 50px;
    width: 90%;
  }
  .aboCon .rt img {
    width: 100%;
  }
  .aboCon .rt .boxLine {
    width: 90%;
    right: 5%;
    top: 0px;
  }
  .aboCon .btn {
    bottom: 35px;
    left: 30px;
  }
  .aboItems {
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    margin: 30px 0;
  }
  .aboItems .item {
    width: 50%;
  }
}
</style>

