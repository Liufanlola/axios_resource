<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
const API_PROXY = 'https://bird.ioliu.cn/v1/?url='
import axios from 'axios'
export default {
  name: 'hello',
  data () {
    return {
      msg: 'vue调用网易云接口',
      musics: []
    }
  },
  mounted: function () {
    axios.get(API_PROXY + 'http://music.163.com/api/playlist/detail?id=19723756')
    .then(function (res) {
      console.log("我是远程代理")
    }, function (error) {
      console.log(error)
    })
  }

}
</script>