README
===========================
一直在学习，感觉提高了，但总是零零碎碎的，最近读了戴明老师的[iOS 开发高手课](#https://time.geekbang.org/column/intro/100024501?tab=intro),受益匪浅 <br/>
先整理下自己的知识体系图 其他的以后再补充

****

|作者|丹飞|
|---|---
|简书|静守幸福|

****
# 目录
* 基础
    - [开发阶段](#开发阶段)
        - [启动流程](#启动流程)
        - [界面布局](#界面布局)
        - [架构设计](#架构设计)
    - [调试测试阶段](#调试测试阶段)
        - [提速调试](#提速调试)
        - [静态分析](#静态分析)
    - [发布阶段](#发布阶段)
        - [自动埋点](#自动埋点)
        - [体积优化](#体积优化)
    - [上线阶段](#上线阶段)
        - [崩溃监控](#崩溃监控)
        - [卡顿监控](#卡顿监控)
        - [日志收集](#日志收集)
        - [性能监控](#性能监控)
        - [多线程问题](#多线程问题)
        - [电量问题](#电量问题)
            
* 应用开发
    - [GUI框架](#GUI框架)
        - [UIKit](#UIKit)
        - [CoreAnimation](#CoreAnimation)
        - [CoreGraphics](#CoreGraphics)
        - [CoreImage](#CoreImage)
        - [OpenGLES](#OpenGLES)
    - [响应式框架](#响应式框架)
        - [ReactCocoa](#ReactCocoa)
        - [RxSwift](#RxSwift)
        - [EasyReact](#EasyReact)
    - [动画](#动画)
        - [Pop](#Pop)
        - [RZTRransitions](#RZTRransitions)
    - [A/B方案](#A/B方案)
    - [消息总线](#消息总线)
        - [PromiseKit](#PromiseKit)
        - [SwiftTask](#SwiftTask)
    - [JSON处理](#JSON处理)
        - [JSONModel](#JSONModel)
        - [Mantle](#Mantle)
        - [JSONDecoder](#JSONDecoder)
    - [布局框架](#布局框架)
        - [Masonry](#Masonry)
        - [SnapKit](#SnapKit)
        - [Cartography](#Cartography)
        - [Yoga](#Yoga)
    - [富文本](#富文本)
        - [YYTest](#YYTest)
        - [DTCoreText](#DTCoreText)
    - [TDD/BDD](#TDD/BDD)
    - [编码规范](#编码规范)

* 原理
    - [系统内核XNU](#系统内核XNU)
    - [AOP](#AOP)
        - [RuntimeMethodSwizzling](#RuntimeMethodSwizzling)
        - [libffi](#libffi)
    - [内存管理](#内存管理)
    - [编译](#编译)

* 原生与前端
    - [JavaScriptCore](#JavaScriptCore)
    - [跨端方案](#跨端方案)
        - [ReactNative](#ReactNative)
        - [Weex](#Weex)
        - [Flutter](#Flutter)
        - [H5](#H5)
    - [布局区别](#布局区别)
        - [原生布局](#原生布局)
        - [前端布局](#前端布局)
    - [渲染区别](#渲染区别)
        - [原生渲染](#原生渲染)
        - [ReactNative渲染](#ReactNative渲染)
        - [Flutter渲染](#Flutter渲染)
    - [动态化方案分析](#动态化方案分析)
        - [WaxPatch](#WaxPatch)
        - [JSPatch](#JSPatch)
        - [OCS](#OCS)
        - [低风险方案](#低风险方案)
  
  -----------
  
## 基础
#### 开发阶段
  启动流程<br/>
  ![App启动流程图](https://user-images.githubusercontent.com/97536164/151513779-8335248d-4740-4b1b-b5d9-96db59de15e0.png)<br/>
  一般情况下，App 的启动分为冷启动和热启动。<br/>
  冷启动是指， App 点击启动前，它的进程不在系统里，需要系统新创建一个进程分配给它启动的情况。这是一次完整的启动过程。<br/>
  对应图中 Not running到Foreground Inactive(很短暂) 到 Active<br/>
  热启动是指 ，App 在冷启动后用户将 App 退后台，在 App 的进程还在系统里的情况下，用户重新启动进入 App 的过程，这个过程做的事情非常少。<br/>
  对应图中 background 到 foreground 启动<br/>
  
  App 的启动时间，指的是从用户点击 App 开始，到用户看到第一个界面之间的时间。总结来说，App 的启动主要包括三个阶段：<br/>
  
  界面布局<br/>
  架构设计
#### 调试测试阶段
  提速调试<br/>
  静态分析
#### 发布阶段
  自动埋点<br/>
  体积优化
#### 上线阶段
  崩溃监控<br/>
  卡顿监控<br/>
  日志收集<br/>
  性能监控<br/>
  多线程问题<br/>
  电量问题
            
## 应用开发
#### GUI框架
  UIKit<br/>
  CoreAnimation<br/>
  CoreGraphics<br/>
  CoreImage<br/>
  OpenGLES
#### 响应式框架
  ReactCocoa<br/>
  RxSwift<br/>
  EasyReact
#### 动画
  Pop<br/>
  RZTRransitions
#### A/B方案
#### 消息总线
  PromiseKit<br/>
  SwiftTask
#### JSON处理
  JSONModel<br/>
  Mantle<br/>
  JSONDecoder
#### 布局框架
  Masonry<br/>
  SnapKit<br/>
  Cartography<br/>
  Yoga
#### 富文本
  YYTest<br/>
  DTCoreText
#### TDD/BDD
#### 编码规范
参考其他公司对 iOS 开发制定的编码规范来完善自己团队的编码规范<br/>比如
![Spotify](#https://github.com/spotify/ios-style) 的 Objective-C 编码规范<br/>
![纽约时报](#https://github.com/NYTimes/objective-c-style-guide)的 Objective-C 的编码规范<br/>
![Raywenderlich](#https://github.com/raywenderlich/objective-c-style-guide) 的 Objective-C 编码规范<br/>
![Raywenderlich](#https://github.com/raywenderlich/swift-style-guide) 的 Swift 编码规范<br/>

按照这几个模板摸索一套自己的代码规范

编码规范的检查

工具检查

如果是 Swift 语言的话，你可以使用 ![SwiftLint](#https://github.com/realm/SwiftLint)工具来检查代码规范。Swift 通过 Hook Clang 和 SourceKit 中 AST 的回调来检查源代码，如何使用 SourceKit 开发工具可以参看这篇文章 ![Uncovering SourceKit](#https://www.jpsim.com/uncovering-sourcekit/)。SwiftLint 检查的默认规则，你可以参考它的 1![规则说明](#https://realm.github.io/SwiftLint/rule-directory.html)。SwiftLint 也支持自定义检查规则，支持你添加自己制定的代码规范。你可以在 SwiftLint 目录下添加一个 .swiftlint.yml 配置文件来自定义基于正则表达式的自定义规则。具体方法，你可以参看官方定义 ![自定义规则的说明](#https://github.com/realm/SwiftLint/blob/master/README_CN.md)。<br/>

如果你是使用 Objective-C 语言开发的话，可以使用 OCLint 来做代码规范检查。关于 OCLint 如何定制自己的代码规范检查，你可以参看杨萧玉的这篇博文 ![使用 OCLint 自定义 MVVM 规则](#http://yulingtianxia.com/blog/2019/01/27/MVVM-Rules-for-OCLint/)

人工检查

人工检查，就是使用类似 Phabricator 这样的 Code Review 工具平台，来分配人员审核提交代码，审核完代码后，审核人可以进行通过、打回、评论等操作。这里需要注意的是，人工检查最容易沦为形式主义，因此为了避免团队成员人工检查成为形式，在开始阶段最好能让团队中编码习惯好、喜欢交流的人来做审核人，以起到良好的示范作用，并以此作为后续的执行标准。<br/>
你可能会有疑问，既然工具可以检查代码规范，为什么还需要人工再检查一遍？我想说的是，工具确实可以通过不断完善，甚至引入 AI 分析来提高检查结果的准确性，但是，我认为 Code Review 之所以最终还是需要人工检查的原因是，通过团队成员之间互相检查代码的方式，希望能够达到相互沟通交流，甚至相互学习的效果。<br/>
试想一下，如果你经过了大量的思考，花费了很多心思写出来一段自认为完美的代码，这时候可以再得到团队其他成员的鼓励，是不是会干劲儿十足呢。相反地，如果你马虎大意，或者经验不足而写出了不好的代码，通过 Code Review 而得到了团队其他成员的建议和指导，是不是能够让你的编码水平快速提高，同时还能够吸纳更多人的经验呢。<br/>Code Review 的过程也能够对代码规范进行迭代改进，最后形成一份能体现出团队整体智慧的代码规范。以后再有新成员加入时，他们也能够快速达到团队整体的编码水平，这就好比一锅老汤，新食材放进来涮涮，很快就有了相同的味道。

## 原理
#### 系统内核XNU
#### AOP
  RuntimeMethodSwizzling<br/>
  libffi
#### 内存管理
#### 编译

## 原生与前端
#### JavaScriptCore
#### 跨端方案
  ReactNative<br/>
  Weex<br/>
  Flutter<br/>
  H5
#### 布局区别
  原生布局<br/>
  前端布局
#### 渲染区别
  原生渲染<br/>
  ReactNative渲染<br/>
  Flutter渲染
#### 动态化方案分析
  WaxPatch<br/>
  JSPatch<br/>
  OCS<br/>
  低风险方案
