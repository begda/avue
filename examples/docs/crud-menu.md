<script>
export default {
    data() {
      return {
        data: [
          {
            name:'张三',
            sex:'男'
          }, {
            name:'李四',
            sex:'女'
          }
        ],
        option:{
          menuWidth:380,
          page:false,
          align:'center',
          menuAlign:'center',
          column:[
             {
              label:'姓名',
              prop:'name'
            }, {
              label:'性别',
              prop:'sex'
            }
          ]
        },
        option1:{
          menu:false,
          page:false,
          align:'center',
          menuAlign:'center',
          column:[
             {
              label:'姓名',
              prop:'name'
            }, {
              label:'性别',
              prop:'sex'
            }
          ]
        },
      };
    }
}
</script>
<style>

</style>

## Crud 模块



### 自定义操作栏

:::demo  有时候我们自定义按钮，操作栏宽度不够，它是不能自适应的,需要设置`menuWidth`属性去改变宽度，同时在`menu`名字的卡槽接受我们自定义的`dom`，返回的`scope`中返回了当前行`row`以及其他我们需要的数据
```html
<avue-crud :data="data" :option="option">
  <template slot-scope="scope" slot="menu">
     <el-button icon="el-icon-check" size="small">自定义菜单按钮</el-button>
  </template>
</avue-crud>

<script>
export default {
    data() {
      return {
        data: [
          {
            name:'张三',
            sex:'男'
          }, {
            name:'李四',
            sex:'女'
          }
        ],
        option:{
          menuWidth:380,
          page:false,
          align:'center',
          menuAlign:'center',
          column:[
             {
              label:'姓名',
              prop:'name'
            }, {
              label:'性别',
              prop:'sex'
            }
          ]
        },
      };
    }
}
</script>
```
:::

### 隐藏

:::demo `menu`属性接受一个`Boolean`的属性达到隐藏的效果，默认为`false`
```html
<avue-crud :data="data" :option="option1"></avue-crud>

<script>
export default {
    data() {
      return {
        data: [
          {
            name:'张三',
            sex:'男'
          }, {
            name:'李四',
            sex:'女'
          }
        ],
        option1:{
          menu:false,
          page:false,
          align:'center',
          menuAlign:'center',
          column:[
             {
              label:'姓名',
              prop:'name'
            }, {
              label:'性别',
              prop:'sex'
            }
          ]
        },
      };
    }
}
</script>
```
:::