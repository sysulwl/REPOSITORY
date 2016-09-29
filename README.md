# 实验报告
**14353104**   **黄新元**

**2016/9/29**

##DOL框架描述
DOL是一种允许应用（半）自主映射到多处理器SHAPES架构平台的框架。

**DOL由下面3部分组成：**

* DOL的API。通过API，可以让开发者在不需要了解底层细节的情况下进行分布式和并行式的编程。
* DOL功能性模拟器。用于提供一个仿真环境供开发者测试程序。
* DOL映射优化。目标是计算这种从应用映射到多处理器SHAPES架构平台的关系。

##DOL安装笔记
* 在ubuntu上安装必要的环境
* 下载必要文件，将压缩包解压到指定目录
* 编译systemc，关键代码是：
  > $../configure CXX=g++ --disable-async-updates

  用途是根据系统配置一些参数。
  然后执行编译，编译完后记录当前工作路径
  > $	sudo make install

* 编译DOL
  修改xml文件

  `<property name="systemc.inc" value="YYY/include"/>`
  `<property name="systemc.lib" value="YYY/lib-linux/libsystemc.a"/>`

  YYY替换为工作路径

  继续编译DOL
  > $	ant -f build_zip.xml all

* 运行实例，最后成功结果如图：
  ![Ubuntu-2016-09-19-11-51-25](https://github.com/portal20/ES2016_14353104/blob/master/Pictures/Ubuntu-2016-09-19-11-51-25.png)


##实验感想

*这两次试验都主要以配置环境为主，另外还学习了MarkDown的使用，收获非常大。*
