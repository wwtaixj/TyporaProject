## vue简介

#### 1.1vue的特性

>  ![image-20211022104610102](.\images\image-20211022104610102.png) 

#### 2.1数据驱动视图

> ![image-20211022105139262](.\images\image-20211022105139262.png)
>
> ![image-20211022105410364](.\images\image-20211022105410364.png)

#### 2.2双向数据绑定

> ![image-20211022105428797](.\images\image-20211022105428797.png)
>
> ![image-20211022111656322](.\images\image-20211022111656322.png)

#### 2.3 MVVM

![image-20211022110229621](.\images\image-20211022110229621.png)

#### 2.4 MVVM的工作原理

![image-20211022111450628](.\images\image-20211022111450628.png)

## vue基础语法

> #### 1. 指令的概念
>
> ![image-20211022113928661](.\images\image-20211022113928661.png)
>
> > ##### 1.1 内容渲染指令
> >
> > > ![image-20211022114137939](.\images\image-20211022114137939.png)
> > >
> > > **v-text **
> > >
> > > ![image-20211022114352587](.\images\image-20211022114352587.png)
> > >
> > > **{{}}语法**
> > >
> > > ![image-20211022134405116](.\images\image-20211022134405116.png)
> > >
> > > **v-html**
> > >
> > > ![image-20211022134755220](.\images\image-20211022134755220.png)
> > >
> > > **总结：**
> > >
> > > ![image-20211022134852475](.\images\image-20211022134852475.png)
> >
> > ##### 1.2 属性绑定指令
> >
> > > ![image-20211025112202769](.\images\image-20211025112202769.png)
> >
> > ##### 1.3 在指令中使用JavaScript语法
> >
> > > ![image-20211025150516867](.\images\image-20211025150516867.png)
>
> #### 2 事件绑定
>
> > ##### 2.1 v-on
>
> > > ![image-20211025150959142](.\images\image-20211025150959142.png)
> >
> > ##### 2.2 $event原生事件对象
> >
> > > ![image-20211025160206851](.\images\image-20211025160206851.png)
> >
> > ##### 2.3 事件修饰符
> >
> > > ![image-20211025160722707](.\images\image-20211025160722707.png)
> >
> > ##### 2.4 按键修饰符
> >
> > > ![image-20211025163803388](.\images\image-20211025163803388.png)
>
> #### 3. 双向绑定
>
> > ##### 3.1 v-model
> >
> > > ![image-20211025171145191](.\images\image-20211025171145191.png)
> >
> > ##### 3.2 v-model 指令的修饰符
> >
> > > ![image-20211025172335018](.\images\image-20211025172335018.png)
>
> #### 4.条件渲染指令
>
> ![image-20211025172813953](.\images\image-20211025172813953.png)
>
> > ##### 4.1 v-if和v-show
> >
> > > ![image-20211025173920600](.\images\image-20211025173920600.png)
> >
> > ##### 4.2 v-else
> >
> > > ![image-20211025174304080](.\images\image-20211025174304080.png)
>
> #### 5.列表渲染指令
>
> > ##### 5.1 v-for
> >
> > > ![image-20211025175107281](.\images\image-20211025175107281.png)
> >
> > ##### 5.2 key
>
> > > ![image-20211026104136362](.\images\image-20211026104136362.png)
>
> #### 6.过滤器
>
> > ##### 6.1 过滤器
> >
> > > ![image-20211026153351098](.\images\image-20211026153351098.png)
> >
> > 注意：过滤器一定要有返回值！
> >
> > ##### 6.2 全局过滤器
> >
> > > ![image-20211026155838549](.\images\image-20211026155838549.png)
> >
> > ##### 6.3 过滤器传参
> >
> > > ![image-20211026164217028](.\images\image-20211026164217028.png)

> #### 7. 侦听器
>
> > #####  7.1 侦听器
> >
> > > ![image-20211026164818435](.\images\image-20211026164818435.png)
> > >
> > > **实例**：
> > >
> > > ​                                                            ![image-20211026174711680](.\images\image-20211026174711680.png)   
> >
> > ##### 7.2 对象格式侦听器(immediate 选项)
> >
> > > ![image-20211026174417658](.\images\image-20211026174417658.png)
> > >
> > > ![image-20211026174500977](.\images\image-20211026174500977.png)
> >
> > ##### 7.3 deep选项
> >
> > > ![image-20211026175657106](.\images\image-20211026175657106.png)
> >
> > ##### 7.4 总结
> >
> > ![image-20211026194532950](.\images\image-20211026194532950.png)

> #### 8.计算属性
>
> > ##### 8.1 计算属性
> >
> > > ![image-20211026180117872](.\images\image-20211026180117872.png)
> >
> > ##### 8.2 总结
> >
> > > ![image-20211026194649348](.\images\image-20211026194649348.png)

> #### 9. axios
>
> > ##### 9.1   基础
> >
> > > ![image-20211026195240318](.\images\image-20211026195240318.png)
> > >
> > > ![image-20211027095941312](.\images\image-20211027095941312.png)
> > >
> > > ![image-20211027095702441](.\images\image-20211027095702441.png)
> >
> > ##### 9.2 async和await方法
> >
> > > ![image-20211027103210797](.\images\image-20211027103210797.png)
> >
> > ##### 9.3 axios.get和axios.post
> >
> > > ![image-20211027104154124](.\images\image-20211027104154124.png)

> #### 10. vue-cli
>
> > ##### 10.1 单页面应用程序
> >
> > > ![image-20211027104326838](.\images\image-20211027104326838.png)
> >
> > ##### 10.2
> >
> > > ![image-20211027143931269](.\images\image-20211027143931269.png)
> > >
> > > ![image-20211027143958501](.\images\image-20211027143958501.png)
> > >
> > > ![image-20211027144007308](.\images\image-20211027144007308.png)
>
> #### 11. 组件
>
> > ##### 11.1 什么是组件化开发
> >
> > > ![image-20211027140552273](.\images\image-20211027140552273.png)
> >
> > ##### 11.2vue的组件化开发
> >
> > > ![image-20211027140629118](.\images\image-20211027140629118.png)
> >
> > ##### 11.3 组件的组成部分
> >
> > > ![image-20211027140800149](.\images\image-20211027140800149.png)
> >
> > ##### 11.4 组件基础
> >
> > > ![image-20211027150749267](.\images\image-20211027150749267.png)
> > >
> > > ![image-20211027152337226](.\images\image-20211027152337226.png)
> > >
> > > ![image-20211027161110440](.\images\image-20211027161110440.png)
> > >
> > > ![image-20211027162114039](.\images\image-20211027162114039.png)
> >
> > ##### 11.5 props 组件传参
> >
> > > ![image-20211027165804528](.\images\image-20211027165804528.png)
> > >
> > > ![image-20211027165647710](.\images\image-20211027165647710.png)
> > >
> > > ![image-20211027170248678](.\images\image-20211027170248678.png)
> > >
> > > ![image-20211027172845655](.\images\image-20211027172845655.png)
> > >
> > > ![image-20211027173749101](.\images\image-20211027173749101.png)

> > ##### 11.6组件间样式冲突

> > ![image-20211027174313118](.\images\image-20211027174313118.png)
> >
> > **解决：**
> >
> > ```javascript
> > <style scoped>//添加scoped属性
> > ```
> >
> > ![image-20211027184649473](.\images\image-20211027184649473.png)
> >
> > ![image-20211027184730665](.\images\image-20211027184730665.png)
> >
> > ##### 11.7 组件实例
> >
> > ：每使用一次组件标签都是new一个组件实例，经过template-compiler插件解析转化为javascript语法再交给浏览器执行。
> >
> > ##### 11.8 组件的生命周期
> >
> > > ![image-20211028100333701](.\images\image-20211028100333701.png)
> > >
> > > ![image-20211028101011659](.\images\image-20211028101011659.png)
> > >
> > > ![image-20211028103025138](.\images\image-20211028103025138.png)
> > >
> > > ![image-20211028105358447](.\images\image-20211028105358447.png)
> > >
> > > ![image-20211028110218479](.\images\image-20211028110218479.png)
> > >
> > > ![image-20211028113317911](.\images\image-20211028113317911.png)
> > >
> > > ![image-20211028113414599](.\images\image-20211028113414599.png)
> > >
> > > *11.8.1*  created 方法
> > >
> > > > ![image-20211028105155737](.\images\image-20211028105155737.png)
> > >
> > > *11.8.2*  mounted 方法
> > >
> > > > ![image-20211028110832064](.\images\image-20211028110832064.png)
> > >
> > > *11.8.3* updated 方法
> > >
> > > > ![image-20211028112239023](.\images\image-20211028112239023.png)
> >
> > ##### 11.9 组件间的数据共享
> >
> > > ![image-20211028133521027](.\images\image-20211028133521027.png)
> > >
> > > ![image-20211028133643235](.\images\image-20211028133643235.png)
> > >
> > > ![image-20211028154144458](.\images\image-20211028154144458.png)
> > >
> > > ![image-20211028160525062](.\images\image-20211028160525062.png)
> > >
> > > ![image-20211028175241704](D:\TyporaProject\images\image-20211028175241704.png)
>
> **总结：**
>
> > ![image-20211029091945220](D:\TyporaProject\images\image-20211029091945220.png)
> >
> > ![image-20211029092211200](D:\TyporaProject\images\image-20211029092211200.png)
> >
> > ![image-20211029093240120](D:\TyporaProject\images\image-20211029093240120.png)
> >
> > ![image-20211029094201882](D:\TyporaProject\images\image-20211029094201882.png)
> >
> > ![image-20211029094659264](D:\TyporaProject\images\image-20211029094659264.png)
>
> > ![image-20211029104307727](D:\TyporaProject\images\image-20211029104307727.png)
> >
> > ![image-20211029110030405](D:\TyporaProject\images\image-20211029110030405.png)
> >
> > ![image-20211029111032036](D:\TyporaProject\images\image-20211029111032036.png)
>
> #### 12.ref 操作DOM
>
> > ![image-20211029113559300](D:\TyporaProject\images\image-20211029113559300.png)
> >
> > ![image-20211029113632876](D:\TyporaProject\images\image-20211029113632876.png)
>
> #### 13.this.$nextTick()方法
>
> > ![image-20211029143315036](D:\TyporaProject\images\image-20211029143315036.png)
>
> #### 14. 数组中的方法
>
> > ##### 14.1 数组中查找元素->.some()方法
> >
> >  ![image-20211029144821907](D:\TyporaProject\images\image-20211029144821907.png)
> >
> > ##### 14.2 数组中查询所有元素是否符合条件->.every()方法
> >
> > ![image-20211029151744791](D:\TyporaProject\images\image-20211029151744791.png)
> >
> > ##### 14.3 数组中累加元素->.reduce()方法
> >
> > **一般实现：**![image-20211029153310435](D:\TyporaProject\images\image-20211029153310435.png)
> >
> > **reduce方法实现：**
> >
> > ![image-20211029155210601](D:\TyporaProject\images\image-20211029155210601.png)
> >
> > ![image-20211029155236674](D:\TyporaProject\images\image-20211029155236674.png)

## 动态组件&异步组件

### 动态组件

- ```javascript
  //缓存失活的组件，使它保持某一状态
  <keep-alive>组件</keep-alive>
  ```

### 异步组件

- ```javascript
  //以工厂函数方式定义组件，需要渲染此组件时，工厂函数异步解析此组件
  //定义1
  Vue.component('saync-example',function(resolve,reject){
      setTimeout(function(){
          //向‘resolve’回调传递组件定义
       resolve({
           template:'<div> is to async</div>'
      })
       },1000)
  })
  //使用1
  Vue.component('async-webpack-example',function(resolve){
      require(['./my-async-component'],resolve);
  })
  //使用2
  Vue.component(
  'async-webpack-example',() => import('./my-async-component'))
  //使用3
  new Vue({
      components:{
          'my-component':()=> import('./my-async-component')
      }
  })
  ```

  

### 子组件访问根组件

```javascript
//获取根组件数据
this.$root.数据键名
//写入根组件数据
this.$root.数据键名=写入数据；
//访问根组件计算属性
 this.$root.属性名
 //调用根组件方法
 this.$root.方法名
```

### 子组件访问父组件

```javascript
this.$parent.
```

### 访问子组件实例或子元素

```

```

