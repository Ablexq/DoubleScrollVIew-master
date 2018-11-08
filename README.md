

###简介
通过behavior实现的类似京东淘宝商品详情页面的上拉下拉页面的切换效果。

![DoubleScrollView](a.gif)
### 测试apk
 [demo.apk](demo.apk)
​	
### 用法

监听

```java
PageContainer pageContainer = (PageContainer) view.findViewById(R.id.container);

pageContainer.setOnPageChanged(new PageBehavior.OnPageChanged(){

    @Override
    public void toTop() {
        //位于第一页
    }

    @Override
    public void toBottom() {
        //位于第二页
    }
});

pageContainer.scrollToBottom()//到第二页
pageContainer.backToTop()//滑动到第一页
```

依赖

1. 依赖doublescrollview library模块或者直接拷贝PageBehavior,Page,PageContainer类和res文件下的文件到项目中。
2. 为coordinatelayout中的作为第二页的组件添加 behavior属性为pagehebavior即可。
3. 具体设置见demo。



### demo引用库
1. [banner](https://github.com/youth5201314/banner):Android广告图片轮播控件，支持无限循环和多种主题，可以灵活设置轮播样式、动画、轮播和切换时间、位置、图片加载框架等


### 参考文章
1. [使用 CoordinatorLayout 实现复杂联动效果](http://www.jianshu.com/p/7f50faa65622)

### License
```
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.```

```