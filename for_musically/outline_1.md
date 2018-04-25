#TRY 1

1.使用至少两种方式实现纯css的自适应搜索框；
2.什么是闭包；
  1）函数作为一个返回值；
  function F1() {
    var a = 100;
    return function() {
      console.log(a); // 自由变量，父作用域寻找
    }
  }
  var f1 = F1();
  var a = 200;
  f1();

  2）函数作为参数传递；
  function F1() {
    var a = 100;
    return function() {
      console.log(a); // 自由变量，父作用域寻找
    }
  }
  var f1 = F1();
  
  function F2(fn) {
    var a = 200;
    fn();
  }
  F2(f1);

3.同源标签之间如何通信；
4.用css画一个三角形；
5.window.onload和document.onload是否是同时执行，为什么；
6.cors请求和普通的http请求有什么区别；
7.请使用数组的reduce方法实现数组的map方法；
8.实现一个rangle函数；
9.请用至少两种方法判断一个对象是否是数组，如何将非数组转化为数组。
10. 严格模式、混杂模式
11. 对SpringMVC有什么理解，优点和缺点
12. 闭包，类和继承
// 闭包实际应用中主要用于封装变量，收敛权限
function isFirstLoad() {
  var _list = [];
  return function (id) {
    if (_list.indexOf(id) >= 0) {
      return false;
    } else {
      _list.push(id);
      return true;
    }
  }
}
// 使用
var firstLoad = isFirstLoad()
firstLoad(10) // true
firstLoad(10) // false
firstLoad(20) // true

13. https 是什么与 http 什么区别
