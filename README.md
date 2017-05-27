#### 关于Android启动页

今天在新项目添加启动页的时候发现一个问题，Activity的启动速度有点慢，而且白屏时间有点久，

我以为是因为使用ConstrainLayout引起的，于是我进行了对比测试后发现，其实并不是，

不过ConstrainLayout是稍微增加了几十毫秒的时间，问题并不是出在这。问题在于Activity继承AppCompatActivity增加了一个Preview的机制，

官方说是给App增加品牌展示Logo使用的。然后我找了几个大厂App测试，发现他们的启动页使用的方式不尽相同，

例如微信，QQ使用的方式是直接禁用掉Preview在主题中使用

    <item name="android:windowDisablePreview">true</item>` 即可。但是有个问题就是，当你点击图标的时候会有一
小段的时间卡顿，才会起来App。感觉体验不是很好。

而网易则是默认显示，也就是让它白屏。
这种方式点击立马会有响应，但是有白屏也不太好看。

而新浪微博则是采用

    <item name="android:windowBackground">@drawable/welcome_layler_drawable</item>当App起来后先显示，
然后在叠加一个一样的页面在上面。

于是我就再找，发现不使用AppCompatActivity，直接使用Activity，就没有这个问题。

####  返回键退出时不结束Activity
    @Override
    public boolean onKeyDown(int keyCode, KeyEvent event) {
        if (keyCode == KeyEvent.KEYCODE_BACK) {
            moveTaskToBack(false);
            return true;
        }
        return super.onKeyDown(keyCode, event);
    }

#### 分析apk包的大小，以及依赖关系，对于apk瘦身还是非常有用的。

AndroidStudio2.2以上开始支持直接打开apk文件。

然后通过gradle 可以查看各个项目依赖了哪些library.

//gradle :project name:dependencies [--configuration compile]

  gradle :app:dependencies --configuration compile

  如下是我分析的结果：


    >gradlew :compiler:dependencies --configuration compile

    Parallel execution with configuration on demand is an incubating feature.

    :compiler:dependencies
------------------------------------------------------------

    Project :compiler
------------------------------------------------------------
    compile - Dependencies for source set 'main'.

    +--- com.google.auto.service:auto-service:1.0-rc2

    |    +--- com.google.auto:auto-common:0.3

    |    |    \--- com.google.guava:guava:18.0

    |    \--- com.google.guava:guava:18.0

    +--- com.squareup:javapoet:1.7.0

    \--- project :annotation


    (*) - dependencies omitted (listed previously)


    BUILD SUCCESSFUL


    Total time: 1.141 secs

可以清晰的看到依赖了哪些包。

