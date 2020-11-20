---
title: DOM
order: 5
nav:
  title: Base
  path: /base
group:
  title: JavaScript
  path: /javascript
  order: 2
---

# DOM

### #什么是 DOM 和 BOM？
dom是文档对象模型，bom是浏览器对象模型
[DOM, DOCUMENT, BOM, WINDOW 有什么区别?](https://www.zhihu.com/question/33453164)
[JavaScript学习总结（三）BOM和DOM详解](https://segmentfault.com/a/1190000000654274#articleHeader21)

---

### #三种事件模型是什么？
DOM0级模型，IE事件模型，DOM2级事件模型
[《一个 DOM 元素绑定多个事件时，先执行冒泡还是捕获》](https://blog.csdn.net/u013217071/article/details/77613706)

---

### #事件委托是什么？
事件代理，动态绑定
[《JavaScript 事件委托详解》](https://zhuanlan.zhihu.com/p/26536815)

---

### #事件捕获和事件冒泡

- 先捕获：window----> document----> html----> body ---->目标元素
- 在冒泡：当前元素---->body ----> html---->document ---->window

---

### #DOM 操作
添加、移除、复制、创建、查找[《原生JS中DOM节点相关API合集》](https://microzz.com/2017/04/06/jsdom/)


### JS实现事件绑定的方法

1. `elementObject.addEventListener(eventName,handle,useCapture) `
2. `elementObject.attachEvent(eventName,handle);`（仅支持IE8及以下）
3. `document.getElementById("demo").onclick = function(){};`

### DOMContentLoad和Load和Finish的区别
- DOMContentLoaded：DOM树构建完成。即HTML页面由上向下解析HTML结构到末尾封闭标签`</html>`
- Load：页面加载完毕。 DOM树构建完成后，继续加载html/css 中的图片资源等外部资源，加载完成后视为页面加载完毕。
- DOMContentLoaded 会比 Load 时间小，两者时间差大致等于外部资源加载的时间。
- Finish：是页面上所有 http 请求发送到响应完成的时间

### 手写遍历DOM树所有节点（非递归）
