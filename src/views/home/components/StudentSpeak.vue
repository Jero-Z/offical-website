<template>
  <div class="pubBg">
    <section class="pubCon stuCon">
      <div class="pubTit">
        <h2>合作伙伴</h2>
        <h3>REFLECTIONS</h3>
      </div>
      <div class="slickBox">
        <vue-slick-carousel v-bind="settings">
          <div class="stubox" v-for="item in stuSpeakList" :key="item.id">
            <img :src="item.head" alt="" />
            <div class="stuText">
              <h3>{{ item.name }}</h3>
              <p>
                {{ item.cont }}
              </p>
            </div>
          </div>
        </vue-slick-carousel>
      </div>
    </section>
  </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel';
import 'vue-slick-carousel/dist/vue-slick-carousel.css';
import '@/assets/VueSlickCarousel.css';
export default {
  components: { VueSlickCarousel },
  data() {
    return {
      //轮播配置
      settings: {
        arrows: true, //左右切换按钮
        dots: false, //分页导航
        autoplay: true, //自动播放
        fade: true, //淡化切换
        speed: 500, //动画时间
        autoplaySpeed: 100000, //间隔时间
      },
      stuSpeakList: [
        {
          id: '001',
          name: '中国气象',
          cont: '行业评价',
          head: 'http://www.shallow-sea.com/Upload/image/202206/20220608112506_1128.png',
        },
        {
          id: '002',
          name: '中国商飞',
          cont: '行业评价',
          head: 'http://www.shallow-sea.com/Upload/image/202206/20220608124512_5180.png',
        },
      ],
    };
  },
};
</script>

<style scoped>
.stuCon {
  padding-bottom: 100px;
}

.slickBox {
  background-color: #ffffff;
  padding: 50px 50px;
}

.stubox {
  display: -webkit-box !important;
  display: -ms-flexbox !important;
  display: flex !important;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  padding: 0 150px;
}
.stubox img {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  border: 2px solid #b09c70;
  padding: 8px;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}
.stuText {
  padding: 30px;
  max-width: 680px;
}
.stuText h3 {
  color: #333333;
  font-size: 18px;
}
.stuText p {
  color: #aaaaaa;
  font-size: 14px;
  margin: 15px 0;
  line-height: 26px;
}

/* 小于1100*/
@media (max-width: 1100px) {
  .slickBox {
    width: 90%;
    margin: auto;
  }
  .stubox {
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
    padding: 0;
  }
  .stubox img {
    width: 100px;
    height: 100px;
  }
  .stuText {
    text-align: center;
    padding: 30px 10px 0 10px;
  }
  .stuText p {
    text-align: justify;
  }
}
</style>