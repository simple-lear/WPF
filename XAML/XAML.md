# XAML

## XAML是什么

XAML是一种从XML派生而来的语言，是一种声明式语言，声明一个标签也就意味着声明了一个对象，对象之间的关系要么并列、要么是包含，全都体现在标签的关系上。

XAML是WPF技术中专门用于设计UI的语言。



## XAML的优点

* XAML可以设计出专业的UI和动画   — **好用**
* XAML不需要专业的编程知识，它简单易懂、结构清晰 — **易学**
* XAML使设计师能直接参与软件开发，随时沟通、无需二次转化 — **高效**
* **真正实现了UI与逻辑的分离**



## UI与逻辑紧耦合带来的后果



UI代码与逻辑代码纠缠在一起称为UI与逻辑的紧耦合，往往带来以下后果：

* 无论是软件的功能还是UI设计有所变化或者是出了bug，都将导致大量代码的修改
* 会让逻辑代码更加难以理解——修改往往比重写更困难，因为在修改之前必须先读懂。
* 重用逻辑代码变成了 Mission Impossible







## WPF应用程序项目结构

新建一个"WPF项目"

![](https://gitee.com/lmdlearn/wpf/raw/master/%E7%AC%AC%E4%B8%80%E5%A4%A9/XAML/Images/1.png)



* Properties：里面的内容是程序要用到的一些资源（如图标、图片、静态的字符串）和配置信息。可以设置窗口的图标。
* References：里面是项目中引用的程序集（.dll文件），大部分是.NET Framework 中的类库
* App.xaml：程序的主体。声明了程序的进程会是谁，同时指定了程序的主窗体（文件中的Application标签的StartupUri属性）。就是程序刚开始执行时显示的窗体。App.xaml.cs是App.xaml的后台代码。
* MainWindow.xaml：程序的主窗体。是主要写代码的地方。MainWindow.xaml.cs 是后台代码。





## XAML命名空间

XAML从XML派生而来，语法格式和XML很像。

使用xmlns特征（属性）来定义名称空间。

语法：

```
xmlns[:可选的映射前缀]="名称空间"
```



![](https://gitee.com/lmdlearn/wpf/blob/master/%E7%AC%AC%E4%B8%80%E5%A4%A9/XAML/Images/2.png)



* 第一个名称空间对应的是与绘制UI相关的程序集，是表示 （Presentation）层面上的东西。
* 第二个名称空间对应XAML语言解析处理相关的程序集，是语言层面上的东西。

第一个xmlns声明的命名空间是没有前缀的，这是默认名称空间。在XAML中，**默认名称空间没有前缀，同时只能有一个**。因为XAML标签大多数都和UI相关，所以将其设为默认名称空间，省去前缀，不然每次写标签还得加个前缀，很麻烦。

后面会学习x名称空间中的内容...







