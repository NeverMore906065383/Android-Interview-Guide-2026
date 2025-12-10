# Android-Interview-Guide-2026
高级 Android 开发工程师面试题目录（大纲）

一、Android 基础能力

1. Java / Kotlin 语言

• Java 基础：集合、并发、多线程、反射、泛型、类加载机制

• Kotlin：协程、扩展、委托、协变/逆变、inline、sealed、data class

• JVM 基础：内存结构、GC 原理、编译与调优

• JMM 内存模型、volatile、锁原理（偏向/轻量/重量）

2. Android 四大组件

• Activity 生命周期完整图（含横竖屏切换、跳转、taskAffinity、singleTask 等）

• Fragment 全部生命周期与内存回收问题

• Service：前台服务、进程保活、bindService 生命周期

• BroadcastReceiver：有序广播、粘性广播、注册差异

• ContentProvider：跨进程访问机制、Binder、Uri 权限

3. UI 与布局系统

• View Measure/Layout/Draw 流程

• 自定义 View（三大流程、事件分发机制）

• 事件分发 dispatch/onIntercept/onTouch

• RecyclerView 原理（回收复用、DiffUtil、viewType 管理）

• ConstraintLayout、MotionLayout

• 触摸、滑动冲突处理

4. 资源管理 & 国际化

• 多分辨率适配

• density / dpi / px / dp 关系

• 多语言切换、资源覆盖原则

二、架构设计能力

1. MVVM / MVI / MVP 架构及差异

• ViewModel + LiveData / StateFlow / SharedFlow

• 数据驱动 UI 的可预测性

• 单向数据流（UDF）

• Jetpack Compose 架构思想

2. Jetpack 体系

• Room（Paging、Flow 支持）

• Navigation（图结构、深链）

• WorkManager（任务调度）

• Lifecycles

• DataStore（preferences vs proto）

3. 模块化 / 组件化 / 插件化

• 模块边界设计

• ARouter / EventBus 的利弊

• 插件化（Replugin、DroidPlugin、Dynamic Feature Module）

• 动态加载（ClassLoader、DexClassLoader）

4. Clean Architecture

• domain/data/ui 分层

• Repository 模式

• 依赖倒置、接口隔离、SOLID 原则

三、Android Framework & 底层知识

1. Binder / IPC

• Binder 机制原理

• AIDL、Messenger、ContentProvider、Socket 区别

• 系统服务（AMS/WMS）整体架构

2. ActivityManager / WindowManager 框架

• Activity 启动流程

• Application 启动流程

• Window 管理、SurfaceFlinger、Choreographer

3. 进程与线程模型

• 主线程 Looper/MessageQueue 原理

• Handler 原理、IdleHandler

• ANR 产生的根源

4. 存储机制

• 沙盒、分区存储

• 外置存储访问权限

• SAF（Storage Access Framework）

四、性能优化能力（关键）

1. 启动速度优化

• 冷启动路径

• Application 冗余初始化优化

• Trace、systrace、startup runtime

2. UI 性能优化

• FPS 卡顿分析（Choreographer、掉帧）

• Layout Inspector / GPU 渲染分析

• View 过度绘制

• 大图优化

3. 内存优化

• OOM 排查、泄漏定位

• LeakCanary 原理

• Bitmap 内存优化（inSampleSize、复用池）

• WeakReference、ReferenceQueue

4. APK 体积优化

• R8、ProGuard 混淆

• 资源裁剪（aapt2、res shrink）

• so 处理（ABI 分包）

• 多 Dex、MultiDex

5. 网络优化

• DNS、HTTP/2、连接池

• OkHttp 拦截器链

• Gson/Moshi 序列化性能差异

五、系统安全与合规

1. Android 权限模型

• 普通权限、危险权限、特殊权限

• 动态权限流程

• 后台权限（后台弹框、后台定位）

2. 应用安全

• 加固原理、ProGuard、R8 工作机制

• 反编译与防逆向（Dex 加密、Code Virtualization）

• WebView 安全、跨域、JS Bridge

3. 数据安全与合规

• GDPR / CCPA 基础

• 国内隐私合规（隐私弹窗、权限最小化、SDK 合规）

• 三方 SDK 合规检测点

六、网络与后端协作能力

1. 网络基础

• Retrofit + OkHttp 源码分析

• WebSocket、心跳机制

• 网络缓存策略（CacheControl）

2. 协程/线程 + 网络结合

• 协程执行器、线程切换

• 流式数据处理（Flow + 网络）

3. GraphQL / gRPC / ProtoBuf

• 与 REST 的差异

• 性能优势

• 使用场景

七、第三方 SDK 与工具链能力

• Firebase / Google Play 服务

• Facebook SDK、Adjust、Appsflyer 集成原理

• 广告 SDK（AdMob / Meta Audience Network）

• 崩溃监控：Crashlytics、Sentry

• 性能监控：BlockCanary、Matrix

八、跨平台与生态

1. Flutter / React Native / Compose 多平台

• Flutter 引擎原理（Platform Channel）

• RN Bridge 模型

• Compose 性能特点

2. NDK / C++ 基础

• JNI 调用流程

• Native 崩溃定位

• so 加载原理

九、工程能力（软实力）

• 软件设计能力

• 项目模块化、架构治理

• 单元测试 / UI 测试 / 集成测试

• Code Review 习惯

• DevOps / CI/CD（GitHub Action、Jenkins）

• 性能监控、线上问题定位（ANR、Crash、耗电、网络）

十、开放性问题（高阶工程师必问）

1. 如何搭建一个公司级的 Android 基础架构？
2. 如何做增量更新、热修复（Tinker、Sophix 原理）？
3. 如果你负责一个从 0 到 1 的 App，你会如何设计整个架构？
4. 你遇到过最难的性能问题是什么，如何解决？
5. 如何治理多人开发带来的架构混乱？
