<template>
  <div class="m-istyle">
    <dl class="movie">
      <dt>猫眼电影</dt>
      <dd class="active">即将上映</dd>
    </dl>
    <el-carousel trigger="click" indicator-position="none" arrow="always" :autoplay="false">
      <el-carousel-item v-for="(item,index) in list" :key="index">
         <ul class="ibody">
            <li v-for="(movie,index) in item" :key="index">
              <img
                :src="movie.image"
                class="image film-img"
              />
              <div class="film">
                <p>
                  <span class="gold">{{ movie.perNum }}</span>人想看
                </p>
                <p>
                  <span class="name">{{ movie.name }}</span>
                </p>
              </div>
            </li>
          </ul>

      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
  data(){
    return {
      list: [
        [{
        image: '//p0.meituan.net/movie/1907a5af889e44236fd80952980d36e13257090.jpg@214w_297h_1e_1c',
        perNum: '5499',
        name: '82号古宅'
      },
      {
        image: '//p1.meituan.net/movie/eb37c5b78ec0c14aaad707700fcc1443390529.jpg@214w_297h_1e_1c',
        perNum: '1120',
        name: '恋上美人鱼'
      },
      {
        image: '//p0.meituan.net/movie/6adbe9c365a3aaadfb65910bc279bf6a3385927.jpg@214w_297h_1e_1c',
        perNum: '645',
        name: '沉香'
      },
      {
        image: '//p1.meituan.net/moviemachine/f31b925aa6febc11140adbba4b966b3f8269247.jpg@214w_297h_1e_1c',
        perNum: '533',
        name: '亲亲哒'
      },
      {
        image: '//p1.meituan.net/moviemachine/e10ceb90d2c06d3524d01d573ccf88fb7514998.jpg@214w_297h_1e_1c',
        perNum: '16631',
        name: '金蟾降魔'
      }],
        [{
        image: '//p0.meituan.net/movie/a06c36755e3e4e902235e9904cc1551b4677926.jpg@214w_297h_1e_1c',
        perNum: '11979',
        name: '印度奇游'
      },

      {
        image: '//p0.meituan.net/movie/0af34ec7025796b7fdac56d6f2ad3554265477.jpg@214w_297h_1e_1c',
        perNum: '4469',
        name: '无风也起浪'
      },
      {
        image: '//p1.meituan.net/movie/174c45cf85694f065224ee38b29282903015976.jpg@214w_297h_1e_1c',
        perNum: '1542',
        name: '愤怒的心'
      },
      {
        image: '//p1.meituan.net/moviemachine/1d2b4985d0187b437d41a73994ba2e191607376.jpg@214w_297h_1e_1c',
        perNum: '6891',
        name: '奇妙亡国之奇旅'
      },
      {
        image: '//p0.meituan.net/movie/81fe2197ef930c79624a28cc76c423835264620.png@214w_297h_1e_1c',
        perNum: '6214',
        name: '小公主艾薇拉与神秘王国2'
      }]
      ]
    }
  }
};
</script>

<style lang="scss">
@import "@/assets/css/index/cone.scss";
</style>


