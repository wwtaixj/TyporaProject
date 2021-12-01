### vue-Router基础

##### 1.定义（路由）组件

```javascript
const component = () => import('url');
```

##### 2.定义路由

每个路由都应该映射一个组件。

```javascript
const routes = [{path: '/component'}];
```

##### 3.创建路由实例

```javascript
const router = new VueRouter({routes:routes}) //routes:routes 相当于 routes;
```

##### 4.挂载根实例

```javascript
const app = new Vue({router}).$mount('#app');
```

