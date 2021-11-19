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
