计算机网络，

```javascript
function f (a) {
    console.log(a); //un
    var a = 123;
    console.log(a); //123
    function a () {
        console.log('a');
    }
    a();
}
f(1);
```