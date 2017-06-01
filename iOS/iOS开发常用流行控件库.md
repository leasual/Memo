
----------------------------------------start ／appsign.io/分析得到各个大厂基本都是用的第三方库---------------------------------------

====界面效果类====

知名公司很多炫酷的动画库  
https://github.com/Yalantis    

https://github.com/Ramotion  

强大的动画库  

https://github.com/MengTo/Spring  

https://github.com/lkzhao/Hero  


常用的动画库带demo  

https://github.com/younatics/MotionBook  

swift工具库集  

https://github.com/keitaoouchi/awesome-swift  

material design库  

https://github.com/CosmicMind/Material  

navigationbar全屏返回 

类似qq带渐变效果  
http://www.jianshu.com/p/454b06590cf1  

https://github.com/EnderTan/ETNavBarTransparent  

全屏手势返回  

https://github.com/forkingdog/FDFullscreenPopGesture  

状态栏变色  

https://github.com/wangrui460/WRNavigationBar  


https://github.com/MoZhouqi/KMNavigationBarTransition  

顶部有图片时，navigation bar透明，然后向上滑动时navigation bar渐变为不透明  

https://github.com/bijuc92/Animating-Navigation-Bar  

--------------------------------------------------------------------------------------------  
36kr使用的就是这个库作为每个vc的导航

越来越多的应用为每一个 VC 设置单独的导航条，而不是之前那样使用一个全局统一的导航条，因为不同的 VC 有不同的视觉样式，前一个是蓝色的，后一个也许要做成红色、透明，或者干脆没有导航条。  

虽然开发者可以在每个 VC 的 - (void)viewWillAppear （想想为什么不是 - (void)viewDidLoad） 方法中设置自己所需的样式，但是在同一个导航条上来回修改，稍不注意就会导致样式混乱。另一种实现方式，是隐藏全局那个导航条，每个 VC 自己通过 addSubview:(UIView *)view 的方式自己设置导航条。这种实现是可行的，但是使用不方便了，如：  

无法使用 self.navigationItem.rightBarButtonItem 等来设置导航按钮，而必须自己手动往 navigationBar 上加；  

无法使用 self.title 来修改导航标题，而必须自己添加监听；  

无法方便地设置 navigationBarHidden；  

无法方便地自动调整 contentInsets。  

等等。  


本项目提供一种透明的方式，让开发者像以前一样使用导航器，同时，每个 push 进来的 VC 有自己独立的导航条。  

https://github.com/rickytan/RTRootNavigationController  


--------------------------------------------------------------------------------------------  


3d效果（A simple, highly customisable, data-driven 3D carousel for iOS and Mac OS）
https://github.com/nicklockwood/iCarousel

Loading圆形进度条  

https://github.com/jdg/MBProgressHUD
https://github.com/SVProgressHUD/SVProgressHUD

圆形下载进度条类似iOS系统主界面上的下载效果  

https://github.com/danielamitay/DACircularProgress

下拉刷新  

https://github.com/CoderMJLee/MJRefresh

collection view 瀑布流  

https://github.com/chiahsien/CHTCollectionViewWaterfallLayout  



文字处理  

https://github.com/TTTAttributedLabel/TTTAttributedLabel

一个设置界面组件  

https://github.com/DavdRoman/Bohr

自带模糊到清晰显示的图片下载库  

https://github.com/pinterest/PINRemoteImage

Facebook物理效果弹性动画  

https://github.com/facebook/pop

TableView Swipe  

https://github.com/MortimerGoro/MGSwipeTableCell  


UITableViewCell 左右滑动出现item项操作  

https://github.com/SwipeCellKit/SwipeCellKit  


毛玻璃效果  

https://github.com/nicklockwood/FXBlurView


TableView没有数据时显示的界面  

https://github.com/dzenbot/DZNEmptyDataSet

TabSwipeNavigation 导航条滑动  

https://github.com/ermalkaleci/CarbonKit

带标题滚动的UICollectionView  

https://github.com/CSStickyHeaderFlowLayout/CSStickyHeaderFlowLayout

Alert  

https://github.com/Sumi-Interactive/SIAlertView

侧滑菜单带毛玻璃效果  

https://github.com/romaonthego/REFrostedViewController

颜色，主题处理  

https://github.com/ViccAlexander/Chameleon
https://github.com/jiecao-fm/SwiftTheme

跟随ScrollerView滑动的Navigationbar Scrollable UINavigationBar that follows the scrolling of a UIScrollView  

https://github.com/andreamazz/AMScrollingNavbar

显示消息在状态栏或者导航栏或者导航栏下方  

https://github.com/hyperoslo/Whisper

图片，视频选择器  

https://github.com/hyperoslo/Gallery

拍摄图片选择器  

https://github.com/hyperoslo/ImagePicker





====工具类====  


UIImageView异步加载和缓存  

https://github.com/rs/SDWebImage 

Gif加载：  

https://github.com/Flipboard/FLAnimatedImage

Zip压缩解压工具  

https://github.com/ZipArchive/ZipArchive

快速的键值对对象缓存  

https://github.com/pinterest/PINCache

文字format处理  

https://github.com/mattt/FormatterKit

SQLite数据库  

https://github.com/ccgus/fmdb

一系列的工具集合  

https://github.com/ibireme/YYKit  

--- 中文介绍 ==============  

YYKit 是一组庞大、功能丰富的 iOS 组件。  

为了尽量复用代码，这个项目中的某些组件之间有比较强的依赖关系。为了方便其他开发者使用，我从中拆分出以下独立组件：  

YYModel — 高性能的 iOS JSON 模型框架。  

YYCache — 高性能的 iOS 缓存框架。  

YYImage — 功能强大的 iOS 图像框架。  

YYWebImage — 高性能的 iOS 异步图像加载框架。  

YYText — 功能强大的 iOS 富文本框架。  

YYKeyboardManager — iOS 键盘监听管理工具。  

YYDispatchQueuePool — iOS 全局并发队列管理工具。  

YYAsyncLayer — iOS 异步绘制与显示的工具。  

YYCategories — 功能丰富的 Category 类型工具库。  


Zxing二维码扫描  

https://github.com/TheLevelUp/ZXingObjC

指纹认证  

https://github.com/kishikawakatsumi/KeychainAccess  

https://github.com/soffes/SAMKeychain



=========Swift==============  


Json解析  

https://github.com/SwiftyJSON/SwiftyJSON

代码布局  

https://github.com/SnapKit/SnapKit

图表  

https://github.com/danielgindi/Charts

map转换为对象  

https://github.com/Hearst-DD/ObjectMapper

网络请求库对Alamofire进行了封装，让我们优雅的发起请求，可以使用RxSwift  

https://github.com/Moya/Moya

RxSwift  

https://github.com/ReactiveX/RxSwift  

----------------------------------------end ／appsign.io/分析得到各个大厂基本都是用的第三方库---------------------------------------  



============================================swift写的一些库==============================================  


Pageview title indicator  

https://github.com/Yalantis/Segmentio  


popup弹出动画  

https://github.com/MarioIannotta/MIBlurPopup  

下拉刷新进度条  

https://github.com/ninjaprox/NVActivityIndicatorView  

pallax header view  

https://github.com/gskbyte/GSKStretchyHeaderView  


卡片滑动选择消失类似tinder  

https://github.com/Yalantis/Koloda  

viewpager中间卡片，点击卡片展开  

https://github.com/Ramotion/expanding-collection   


collectionview带动画类似viewpager  

https://github.com/KelvinJin/AnimatedCollectionViewLayout  


类似pinterest点击图片展开到下一个全屏的显示界面  

https://github.com/demonnico/PinterestSwift  


文字随机出现  

https://github.com/zipme/RQShineLabel  


图表支持svg  

https://github.com/exyte/Macaw  

渐变背景 

https://github.com/cruisediary/Pastel  

类似spinner  

https://github.com/younatics/YNDropDownMenu  

侧滑菜单  

https://github.com/jonkykong/SideMenu  

tabbar  底部tab  

https://github.com/Ramotion/animated-tab-bar  


类似最美app底部，宝宝在路上日历中间选择的比较大的效果  

https://github.com/ltebean/LTInfiniteScrollView-Swift  































