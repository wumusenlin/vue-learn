# vue-learn
<div id="app"> 
  <ul> 
    <li v-for=”item in items“>{{ item }}</li> 
   </ul>
</div>
data：{
  items：[1，2， 3， 4]

}
v-for 可以循环的把数组中的数据按列表展示出来
！axios是vue中封装的ajax，其具体用法先引入.<script src="https://unpkg.com/axios/dist/axios.min.js"></script>
[javascript](new Vue({
  el: '#app',
  data () {
    return {
      info: null
    }
  },
  mounted () {
    axios
      .get('https://www.runoob.com/try/ajax/json_demo.json')
      .then(response => (this.info = response))
      .catch(function (error) { // 请求失败处理
        console.log(error);
      });
  }
}))
