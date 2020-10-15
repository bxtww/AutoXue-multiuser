# 写在最前
这个项目完全是为了学习python，学习了原AutoXue的项目，项目地址 https://github.com/kessil/AutoXue
因为原作者没有更新，因此拿来作为研究学习之用，请遵守开源许可协议。严禁用于商业用途，禁止使用进行任何盈利活动。对一切非法使用所产生的后果，本人概不负责。
# 使用方法，一定要先读！！
1、配置环境，参考原作者的配置教程，这点非常重要

2、运行setup.cmd,如果安装不上相关组件，用记事本打开查看命令，手动拷贝到cmd里逐条运行

3、用户名在default.ini里配置，可以配置多用户，也可以单用户。一定要配置！！

4、如果是新的模拟器第一次登录，必须提前登录用一次，把各种提示刷没了，否则app提示操作会导致程序崩溃；

5、进入APP读取分数失败的问题，夜神模拟器安卓版本降到5，目前android7会出现上述问题


# 2020年10月10日
1、修复了阅读bug，目前测试无问题

# 2020年10月8日
1、修复了若干bug，目前版本争上游答题效率优化的比较好了，通过测试80%以上概率夺冠。当然星星越高难度越大，因为要检索文件，肯定赶不上刷题狂，那些高星用户，都是看了题目就本能反应答案的，干不过他们。

2、题库目前运行相对稳定了

3、下一步开发目标，把题库json文件改为sqlit数据库，提高检索效率，把争上游再优化。

4、目前版本阅读有时候不能达到满分，主要问题是之前读过的文章，再怎么读也不给分，解决办法：手动点到要闻或者其他新闻栏目，进去找文章继续刷。这块进行了优化，阅读时间60秒，默认读9篇，应该可以满分了。

5、关于setup文件和start文件，我也是照搬原作者的文件，可能是用的notepad++编辑的问题，不能跑起来，找到原作者的文件自行修改吧。
# 2020年10月4日
1、重新修改了题库，去掉了模糊比对，提高比对效率

2、增加了本地题库更新功能

# 2020年10月1日
1、增加了专项答题功能，这块功能因为没有题库，完全是利用正则表达式匹配的提示内容，因为提示的内容千奇百怪，没法做到100%识别正确。默认关闭，不介意错误的自行修改配置
special_topic = enable

2、关于争上游和双人对战，我限制的目的就是让争上游使用频率降下来，尽量克制，如果总是夺冠，就离被封杀差不多了。

3、关于争上游搞不过别人的问题，因为采用了模糊比对的方法，如果要提高刷分效率，一定要安装python-Levenshtein；
参考：https://zhuanlan.zhihu.com/p/53135935

https://blog.csdn.net/sky_limitless/article/details/90291893
如遇安装python-Levenshtein失败，参考上面链接的“5. 第二种尝试 直接下载 .whl文件，直接安装”，但是注意自己安装的Python版本，如Python是3.8版本就需要下载对应的“Levenshtein-0.12.0-cp38-cp38m-win_amd64.whl”然后就可以顺利安装。(感谢tonylemon提供)

4、有的网友start提示错误，我重新修改了python命令，各位一定要配置环境变量python，按照原作者的说明配置好。
# 2020年9月30日
1、增加了双人对战

2、增加了APP死循环退出功能

3、目前争上游和双人对战还是太过于出风头，建议只刷一个账号就行了，暂不开放多账号刷分了，录入多个号码也是单个循环。

# 2020年9月29日
1、增加了争上游答题，目前还不是很稳定，而且面对刷题狂，无法确保100%战胜对手。

2、通过一段时间的运行，调整了APP反复重启的问题，修复了部分死循环问题，基本上能够启动一次刷完所有账号。


# 2020年9月19日
1.增加了多用户支持，如果是新设备第一次登录，必须提前登录用一次，把各种提示刷没了，否则app提示操作会导致程序崩溃；用户名在default.ini里配置，可以配置多用户，也可以单用户。

2.适配最新版本的学习强国APP，挑战答题的地址也修改了。

3.删除了每周答题和专项答题，这块不是高频应用，且容易出问题，所以暂时屏蔽

4.增加了本地题库，因为题库不全以及个别题目不准，采用题目模糊比对的方式查询答案，多循环几次肯定能完成挑战答题。

5.为了提高刷分效率，我把看文章和视频的时间都压缩了，可能耗费时间的项目不能刷满分，各位可以在程序里调整。

另外，不写代码10多年了，对python也是不熟悉，很多句式和函数都是现学现用，代码质量不高，bug在所难免，各位多提意见。反馈错误带图加最后几段log，在logs文件夹里。

## 免责申明
`AutoXue`为本人`Python`学习交流的开源非营利项目，仅作为`Python`学习交流之用，使用需严格遵守开源许可协议。严禁用于商业用途，禁止使用`AutoXue`进行任何盈利活动。对一切非法使用所产生的后果，本人概不负责。


0. 如果之前添加过环境变量`ADB1.0.40`请确保删除之

1. 安装`JDK`，本文使用JDK1.8
    + 在环境变量中新建`JAVA_HOME`变量，值为JDK安装路径，如`C:\Program Files\Java\jdk1.8.0_05`
    + 新建`CLASSPATH`变量，值为`.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar;`
    + `Path`变量中添加：`%JAVA_HOME%\bin和%JAVA_HOME%\jre\bin`
    
2. 安装`SDK`，本文使用SDK r24.4.1
    + 在环境变量中新建`ANDROID_HOME`，值为SDK安装路径，如`C:\Program Files (x86)\Android\android-sdk`
    + 在Path变量中添加项：`%ANDROID_HOME%\platform-tools` 和 `%ANDROID_HOME%\tools`
    + 打开`SDK Manager.exe` 安装对应的工具和包,根据安卓版本进行安装，**Tools**和**Build-tools**别漏
    ![avatar](https://github.com/kessil/AutoXue/raw/dev/image-20200601204634969.png)
    
3. 安装`Appium-desktop`，为了使用`UiAutomator2`，请将`Appium`设为以管理员权限启动，并赋予JDK和SDK所有权限
    ![avatar](https://github.com/kessil/AutoXue/blob/dev/image-20200601204913532.png)
    

4. 安装一个模拟器，就选夜神Nox吧，如用其他模拟器或真机出现问题请自救。

5. 安装`Python`，请至少使用3.7+版本，推荐3.8

## 使用方法(windows)
0. 克隆项目 `git clone https://github.com/SpringCity-LaoYang/AutoXue-multiuser.git --depth 1`
1. 双击运行`setup.cmd`
2. 启动 `Appium` 和 `Nox`
3. 双击运行 `start.cmd`

