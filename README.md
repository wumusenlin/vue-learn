### vue-learn
```
  <div id="app"> 
    <ul> 
      <li v-for=”item in items“>{{ item }}</li> 
     </ul>
  </div>
  javascript
  data：{
    items：[1，2， 3， 4]
  }
```
v-for 可以循环的把数组中的数据按列表展示出来
！axios是vue中封装的ajax，其具体用法先引入.`<script src="https://unpkg.com/axios/dist/axios.min.js"></script>`

  ```
  var senlin new Vue({
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
  ```
  
#### 有两条下划线的类需要在<style lang="less"></style>中修改样式，非全局不起作用，为避免样式污染，要在需要改的类上添加外层容器的类
```
.warp{
    .container{
      backgroundcolor: red;
    }
  }
```
#### vue中定义一个组件时候（也就是test.vue这样的文件）时候template中必须且有唯一的div 如下：
  
  ```
  <template>
    <div class="test"> 
    </div>
  </templata>
``` 
#### vuejs中在定义函数时使用data里的数据需要加上this,在一个函数中使用另一个函数同理
#### vue项目中遇到报错：希望的值是number类型拿到的确实string类型，可能是绑定的关键字没加‘ ：’符号 
#### vue中自定义组件需要子组件
  ``` 
      export default {
        name: "planDetialDig",
      }
  ```
 #### 并且父组件
 ```
  import planDetialDig from'../overview/plandetial-dig.vue'
    export default {
        components: {
            planDetialDig,
        },
      }
      //使用
      <template>
        <planDetialDig> </planDetialDig>
      </template>
 ```
#### v-if && v-else-if && v-els 用法: v-if不成立判断紧接着的v-else，有多次判断的在两者间加v-else-if。如下理解为status的判断顺序为v-if 齐次v-else-if最后v-else
  ``` 
  <div v-if="status == 'loading'"> 
        <div style="background-color:blue">loading</div>
    </div>

    <div v-else-if="status === 'success'">
        <div style="background-color:green">success</div>
    </div>

    <div v-else>
        <div style='background-color:red'>fail</div>
    </div>
    ```
