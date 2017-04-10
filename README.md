#### 关于Android启动页

今天在新项目添加启动页的时候发现一个问题，Activity的启动速度有点慢，而且白屏时间有点久，

我以为是因为使用ConstrainLayout引起的，于是我进行了对比测试后发现，其实并不是，

不过ConstrainLayout是稍微增加了几十毫秒的时间，问题并不是出在这。问题在于Activity继承AppCompatActivity增加了一个Preview的机制，

官方说是给App增加品牌展示Logo使用的。然后我找了几个大厂App测试，发现他们的启动页使用的方式不尽相同，

例如微信，QQ使用的方式是直接禁用掉Preview在主题中使用

`<item name="android:windowDisablePreview">true</item>` 即可。但是有个问题就是，当你点击图标的时候会有一
小段的时间卡顿，才会起来App。感觉体验不是很好。

而网易则是默认显示，也就是让它白屏。
这种方式点击立马会有响应，但是有白屏也不太好看。

于是我就再找，发现不使用AppCompatActivity，直接使用Activity，就没有这个问题。




