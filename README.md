----
本库是基于RecyclerViewHeader的扩展。
###RecyclerView头View的ViewGroup，支持与WebView，Video,View 嵌套使用

# 特性
1. 解决webView在RecyclerView中的滑动冲突和点击事件
2. 增加滑动RecyclerView中视频为小屏模式（功能参考美拍）
3. 优化过渡绘制卡的问题

#还未完善的问题
1. RecyclerView和webView之间切换时滑动完美  但两个之间的滑动惯性传递不是很完美
（欢迎留言惯性的优化方案）

### Demo
可以下载Demo查看。
[Download](https://github.com/mengzhidaren/RecylerViewMultiHeaderView/blob/master/apk/debug/app-debug.apk?raw=true)
# 截图
## HeaderVideo  HeaderView   
<image src="./img/111.gif" width="300px"/>  <image src="./img/222.gif" width="300px"/>  
## HeaderWebView
  <image src="./img/333.gif" width="300px"/>
  
## 引入
* Gradle
```groovy
compile 'com.yyl.multiview:recyclerview-multiheaderview:1.0.7'
```

## 开发
在xml中引用RecyclerViewMultiHeader：
```xml
    <com.yyl.multiview.RecyclerViewMultiHeader
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            app:viewState="video"
            app:videoScale="0.5625">//video 9/16
....
        </com.yyl.multiview.RecyclerViewMultiHeader>
    
    
    
```

```
// 设置视频监听。
    //视频小窗口开关
   public void setScreenSmallDisable(boolean stateVideoSmallDisable)
    //视频小窗口监听
   public void setOnVideoSmallCallBack(OnVideoSmallCallBack onVideoSmallCallBack)

```

### 参考代码
* [RecyclerViewHeader](https://github.com/blipinsk/RecyclerViewHeader)

本库的是以RecyclerViewHeader为基础在功能上做的扩展，感谢作者开源库。


## License
[MIT License](https://opensource.org/licenses/MIT).
