# jquery.scrollFixedBottom
## 问题描述
当页面内容有横向滚动条，同时数据很长使得横向拖动滚动条的时候需要将页面滑动至滚动条出现的地方，用户体验不好，因此写此小插件解决该问题。

## 问题解决
页面内容的横向滚动条一直出现在用户可操作范围内，提升用户体验。

## 快速体验
https://shinne.github.io/jquery.scrollFixedBottom/index.html

## 外部依赖
jquery.js

## 快速上手
* 引入jquery.js和scrollFixedBottom.js
* 可能出现横向滚动条的div.scroll-wrap及宽度很宽的内容div.scroll-item:
~~~html
    <div class="scroll-wrap" style="overflow-x:scroll;width:800px;">
        <div class="scroll-item" style="width:3000px;height:3000px;"></div>
    </div>
~~~
* 初始化该插件:
~~~javascript
    new ScrollFixedBottom();
~~~
## 配置参数
  ### options
  字段 | 类型 | 默认值 | 说明
  ------------- | ------------- | ------------- | -------------
  scrollWrapEle | String | ".scroll-wrap" | 具有横向滚动条的外层包裹器
  scrollItemEle | String | ".scroll-item" | 需要被横向滚动的真正元素
  left | Number | 0 | 初始化时需要横向滚动的左偏移量

## 方法
* ### var scrollFixed = new ScrollFixedBottom(options)
  通过options配置，初始化该插件，并返回该插件的实例
* ### scrollFixed.refresh(options)
  异步加载数据或者需要横向滚动的数据发生变化时，重新渲染该横向滚动条
* ### scrollFixed.reload()
  当滚动数据发生display属性变化时调用该方法




