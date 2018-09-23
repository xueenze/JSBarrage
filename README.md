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

# CSS样式
```css
.barrage-container{
    height: 3rem;
    overflow: hidden;

    .barrage-item{
        position: absolute;
        left: 100%;
        white-space: nowrap;
        color : #cac8d2;
        padding-right : 1em;
        font-weight: lighter;
        display: inline-flex;
        align-items: center;
        background-color: rgba(216, 235, 255, 0.3);
        border-radius: 0.5rem;

        img{
            width: 0.6rem;
            height: 0.6rem;
            border-radius: 50%;
            margin-right: 0.1rem;
        }
    }

    .barrage-item[data-rank = "0"]{
        top:3%;
    }

    .barrage-item[data-rank = "1"]{
        top:27%;
    }

    .barrage-item[data-rank = "2"]{
        top:52%;
    }

    .barrage-item[data-rank = "3"]{
        top:77%;
    }
}
```
