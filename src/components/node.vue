<template>
  <div class="curl">
    <h1>{{ msg }}</h1>
  </div>
</template>
<script>
export default {
  name: 'curl',
  data () {
    return {
      msg: 'vue调用网易云接口',
    }
  },
  mounted: function () {
    this.$http.get('/api/v2/movie/in_theaters', {}, {
      headers: {

      },
      emulateJSON: true
    }).then(function (res) {
      console.log(res)
    }, function (error) {
      console.log(error)
    })
  }
}
</script>