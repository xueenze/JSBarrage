# JSBarrage
基于jquery的弹幕墙

# 效果图
![](https://github.com/xueenze/JSBarrage/blob/master/demo.png)

# 引入方式
这里的引入是基于Jquery和ES6的语法的，其中关于es6的语法完全可以替换成ES5的语法，看客们自己改就好了！

```js
// 开始弹幕
var barrage = new Barrage({
    wrapper : $('.barrage-container'),
    rank : 3,
    speed : 1.5,
    tmp : function(data, rank){
        return `<div class = "barrage-item" data-rank = '${rank}'>
          <img src = '${data.img}'><span>${data.content}</span></div>`;
    },
    data : displayData,
    distance : 10
});

barrage.begin();
```
