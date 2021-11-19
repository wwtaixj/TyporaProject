**Array 注意项：**

1. <span style='color:red'>*请注意*</span>，直接给`Array`的`length`赋一个新的值会导致`Array`大小的变化！

2. <span style='color:red'>*请注意*</span>，如果通过索引赋值时，索引超过了范围，同样会引起`Array`大小的变化！

3. `slice()`就是对应String的`substring()`版本，它截取`Array`的部分元素，然后返回一个新的`Array`：

   ```javascript
   var arr = ['A', 'B', 'C', 'D', 'E', 'F', 'G'];
   arr.slice(0, 3); // 从索引0开始，到索引3结束，但不包括索引3: ['A', 'B', 'C']
   arr.slice(3); // 从索引3开始到结束: ['D', 'E', 'F', 'G']
   ```

   <span style='color:red'>注意到</span>`slice()`的起止参数包括开始索引，不包括结束索引。

   如果不给`slice()`传递任何参数，它就会从头到尾截取所有元素。利用这一点，我们可以很容易地复制一个`Array`：

   ```javascript
   var arr = ['A', 'B', 'C', 'D', 'E', 'F', 'G'];
   var aCopy = arr.slice();
   aCopy; // ['A', 'B', 'C', 'D', 'E', 'F', 'G']
   aCopy === arr; // false
   ```

4. *请注意*，`concat()`方法并没有修改当前`Array`，而是返回了一个新的`Array`

**Object 注意：**

1. 如果属性名包含特殊字符，就必须用`''`括起来，访问这个属性也无法使用`.`操作符，必须用`['xxx']`来访问。

**if...else 判断注意：**

1. JavaScript把`null`、`undefined`、`0`、`NaN`和空字符串`''`视为`false`，其他值一概视为`true`，因此上述代码条件判断的结果是`true`。

**for 循环注意：**

1. *请注意*，`for ... in`对`Array`的循环得到的是`String`而不是`Number`。

**函数注意：**

1. JavaScript还有一个免费赠送的关键字`arguments`，它只在函数内部起作用，并且永远指向当前函数的调用者传入的所有参数。`arguments`类似`Array`但它不是一个`Array`

2. ```javascript
   // 交换两个数
   b=[a,a=b][0];
   a=a+b-(b=a);
   a=a^b;
   b=b^a;
   a=a^b;
   ```

3. **对于this指向改变的五点：**
   1. 检查 ' . ' 左边是谁invoke 这个函数. 例如 xiaoming.age(); age函数里面有this, 然后 '. ' 旁边是xiaoming , 那么this就是指向xiaoming了.这种叫做 Implicit Binding.
   2. 如果点旁边没有,那就检查有没有用到 bind, apply, call 这三种, 有的话就是调用此方法的对象. 这种叫做 explicit binding.
   3. 如果上面两个都没有就检查代码里面有没有用到new 这个keyword, 有的话那就是指向new旁边的函数对象. 这种叫做new binding
   4. 上面三个都没有, 检查是不是有arrow function, 有arrow function的话就是, 那么指向是arrow function的lexical binding 的对象. 就是她的parent. 这种叫做 lexical binding
   5. 全部都没有如果不是strict mode那就是window对象了.. strict就是 error (undefined).

**高阶函数注意：**

1. `Array`的`sort()`方法默认把所有元素先转换为String再排序，默认是ASCII码从低到高
2. `sort()`方法会直接对`Array`进行修改，它返回的结果仍是当前`Array`。

**闭包：**

1. 每次调用闭包返回函数都会返回一个新的函数，即使传入相同的参数。
2. 返回闭包时牢记的一点就是：返回函数不要引用任何循环变量，或者后续会发生变化的变量。

**箭头函数注意：**

1. 箭头函数完全修复了`this`的指向，`this`总是指向词法作用域，也就是外层调用者。
2. 箭头函数不会创建自己的`this,它只会从自己的作用域链的上一层继承this`

**Date对象：**

1. JavaScript的Date对象月份值从0开始，牢记0=1月，1=2月，2=3月，……，11=12月。
2. 使用Date.parse()时传入的字符串使用实际月份01~12，转换为Date对象后getMonth()获取的月份值为0~11。

**对象的注意项：**

1. 

2. ```javascript
   function Student(name) {
       this.name = name;
       this.hello = function () {
           alert('Hello, ' + this.name + '!');
       }
   }
   var xiaoming = new Student('小明');
   xiaoming.name; // '小明'
   xiaoming.hello(); // Hello,小明!
   xiaoming.constructor === Student.prototype.constructor; // true
   Student.prototype.constructor === Student; // true
   
   Object.getPrototypeOf(xiaoming) === Student.prototype; // true
   
   xiaoming instanceof Student; // true
   ```

**原型链继承：**

1. 

2. ```javascript
   function Student (props) {
       this.name = props || '小米'
       this.school = '北大附小！'
   }
   Student.prototype.hello = function () {
       alert("Hello" + this.name + '!')
   }
   // PrimaryStudent构造函数:
   function PrimaryStudent(props) {
       Student.call(this, props);
       this.grade = props.grade || 1;
   }
   
   // 空函数F:
   function F() {
   }
   
   // 把F的原型指向Student.prototype:
   F.prototype = Student.prototype;
   
   // 把PrimaryStudent的原型指向一个新的F对象，F对象的原型正好指向Student.prototype:
   PrimaryStudent.prototype = new F();
   //PrimaryStudent.prototype = new Student();
   // 把PrimaryStudent原型的构造函数修复为PrimaryStudent:
   PrimaryStudent.prototype.constructor = PrimaryStudent;
   
   // 继续在PrimaryStudent原型（就是new F()对象）上定义方法：
   PrimaryStudent.prototype.getGrade = function () {
       return this.grade;
   };
   
   // 创建xiaoming:
   var xiaoming = new PrimaryStudent({
       name: '小明',
       grade: 2
   });
   console.log(xiaoming.name.name); // '小明'
   console.log(xiaoming.grade); // 2
   console.log(xiaoming.school); // 2
   
   // 验证原型:
   console.log(xiaoming.__proto__ === PrimaryStudent.prototype); // true
   console.log(xiaoming.__proto__.__proto__ === Student.prototype); // true
   
   // 验证继承关系:
   console.log(xiaoming instanceof PrimaryStudent); // true
   console.log(xiaoming instanceof Student); // true
   ```

3. 实现函数继承有四种方法：

     1、创建空函数作架桥函数，原理如上代码所示，将其封装成inherits函数

     2、利用create方法， child.prototype=Object.create(parents.prototype)

     3、利用_proto_属性， child.prototype._proto_=parents.prototype

     4、利用setPrototypeOf方法， child.prototype=Object.setPrototypeOf(parents.prototype)

     总结：原型继承的目的是子函数的原型继承父函数的原型，子函数的实例既可以调用子函数原型中的属性，也可以调用父函数原型中的属性； 4种方法本质上都是用父函数的原型创造出子函数的原型，第一个种方法创建架桥函数是为了防止继承父函数实例的属性，这样就违背了原型继承的目的； 2、3、4方法本质上一样，利用JS提供的属性方法直接建立子父函数的继承关系。

**navigator:**

1. navigator.appName：浏览器名称；
2. navigator.appVersion：浏览器版本；
3. navigator.language：浏览器设置的语言；
4. navigator.platform：操作系统类型；
5. navigator.userAgent：浏览器设定的`User-Agent`字符串。

**screen:**

1. screen.width：屏幕宽度，以像素为单位；
2. screen.height：屏幕高度，以像素为单位；
3. screen.colorDepth：返回颜色位数，如8、16、24。

**location:**

1. 可以用`location.href`获取。要获得URL各个部分的值，可以这么写：

   ```javascript
   location.protocol; // 'http'
   location.host; // 'www.example.com'
   location.port; // '8080'
   location.pathname; // '/path/index.html'
   location.search; // '?a=1&b=2'
   location.hash; // 'TOP'
   ```

**document:**

1. `document`对象表示当前页面。由于HTML在浏览器中以DOM形式表示为树形结构，`document`对象就是整个DOM树的根节点。

   `document`的`title`属性是从HTML文档中的`<title>xxx</title>`读取的，但是可以动态改变：

   ```javascript
   document.title = '努力学习JavaScript!';
   ```

2. `document`对象还有一个`cookie`属性，可以获取当前页面的Cookie。

   Cookie是由服务器发送的key-value标示符。因为HTTP协议是无状态的，但是服务器要区分到底是哪个用户发过来的请求，就可以用Cookie来区分。当一个用户成功登录后，服务器发送一个Cookie给浏览器，例如`user=ABC123XYZ(加密的字符串)...`，此后，浏览器访问该网站时，会在请求头附上这个Cookie，服务器根据Cookie即可区分出用户。

   Cookie还可以存储网站的一些设置，例如，页面显示的语言等等。

   JavaScript可以通过`document.cookie`读取到当前页面的Cookie：

   ```javascript
   document.cookie; // 'v=123; remember=true; prefer=zh'
   ```

**history:**

1. 
