# 扩大福窗口探测

## 扩大福窗口探测 2.8.625
> 使用c++开发, 用爱发电, 所以更新时间跨度大, 驱动部分使用C语言开发  
> 类似 spy++的功能, 拖拽探测窗口, 显示窗口一些基础信息, 加入更多人性化的功能  
> 目前最新版 2.7, 加入了调用驱动的功能, 目前只使用了打开进程功能, 可以打开 0x10010 这个窗口所在的进程, 进程名为 csrss.exe  
> 驱动是使用c语言开发, 目前的功能就是一些内存读写/注入/进程保护/枚举模块等比较基础的功能  
> 还加入了 hex/asm  查看器, 可以将查看的内存转换成汇编显示  
> 还有 PE 查看器, 还可以在 PE 查看器内查看模块的导入表/导出表等信息  
>
> 
### 本软件的亮点功能
本软件的亮点:
> 1. 支持x86/x64进程, x86/x64系统
> 2. 使用R0级打开进程, 没有驱动保护的窗口对应的进程都可以查看进程信息
> 3. 消息监控可以自定义消息配色
> 4. 可以查看进程模块的内存、模块的PE结构、导出表、导入表、内存对应的汇编代码等
> 5. 可以查看窗口子项目信息, 比如列表类组件, 可以查看各个项目的详细信息
> 6. 拖拽查看窗口更人性化, 主界面显示选中窗口的更多信息, 下面的分组还支持查看更多详细的信息
> 7. 可以查看窗口所在进程使用的模块列表, 可以枚举Prop属性, WindowLong, ClassLong的值
> 8. 窗口树会根据窗口状态显示不同的颜色, 窗口状态一目了然
> 9. 可以对目标窗口发送窗口消息、线程消息
> 10.动态增删窗口样式/修改父窗口/修改 ID
> 11.查看窗口4个边的非客户区尺寸
> 12.拖拽调整目标窗口的尺寸位置

### 后续更新计划
> 1. 发送消息支持输入常量,支持模糊输入  
> 2. 发送消息的消息支持打开消息查看器获取   
> 3. 发送消息的参数支持发送结构  
> 4. 查看窗口子信息做全,各类常见组件都需要完成  
> 5. 生成常用代码,包括创建窗口常用功能执行后生成对应代码  
> 6. 把 PE 目录表所有的表都弄出来  
> 7. 



## 历史更新日志

2024-06-25 2.8.702 测试版 更新日志  
修复:  
    1. 优化导出表导入表功能  
    2. PE查看/导入/导出表 支持拖放文件查看  
    3. 功能菜单里 解除禁止按钮/显示隐藏控件 不能处理的问题   
    4.   
新增:  
    1. 搜索导出表函数名/地址  
    2. 搜索导入表函数名/地址/函数序号  
    3. 增加spy_module.exe文件, 解析后的PE会记录起来, 使解析PE加速  
    4.   

2024-04-19 2.7.419 测试版 更新日志  
修复:  
    1. 右键 重新加载该窗口 崩溃的问题  
    2. 消息监控可能出现崩溃的问题  
    3. win7下无法运行的问题  
    4.   
  
  
2024-03-15 2.6.315 更新日志  
修复:  
    1. 窗口树图标空白的问题  
    2. 修复获取进程被挂起的窗口导致死锁的问题  
    3. 修复其他已知问题  
    4.   
新增:  
    1. 全部窗口DPI适配  
    2. 新增深色主题  
    3. 消息监控支持标记颜色, 支持搜索跳转  
    4. 导出表新增显示函数在内存中的前几个字节, 和在文件中的前几个字节, 用于判断是否被hook  
    5. 导出表/导入表 新增常用菜单, 跳转/搜索功能  
    6. 模块信息分类下新增查看数据表快捷菜单  
    7. 如果窗口所在的进程是管理员权限启动, 则在窗口树最顶层的窗口图标显示小盾牌  
    8. 类样式/窗口样式/扩展样式/控件样式/控件扩展样式 新增排序功能  
    9. 导出表增加了排序功能, 点击对应表头可进行排序操作  
   10. 查看子组件信息支持获取虚表标题, 虚表有通过 LVN_GETDISPINFO 返回标题的才能获取  
   11.   
优化:  
    1. 优化窗口树显示速度  
    2.   
          
2023-12-16 2.5.1216 更新日志  
修复:  
    1.   
新增:  
    1. DPI缩放适配  
    2. 消息监控, 消息过滤, 消息解析  
    3.   
      
2023-07-09 2.4.709 更新日志  
移除:  
    1. 移除自绘滚动条, 和原版没太大差别, 还不如就使用原版  
    2.   
修复:  
    1. 修复窗口树选中窗口是无效时无法探测的问题  
    2. 修复查看子项目的一些问题  
    3. 修复消息监控失效的问题  
    4.   
新增:  
    1. 探测加入了缓动效果  
    2. 新增内存查看器, 可以在窗口树查看内存, 也可以在模块查看指定模块内存  
    3. 新增汇编查看器, 在内存查看器中右键选择跳转到汇编窗口即可查看  
    4. 新增PE查看器, 在模块中可以查看指定模块的PE结构  
    5. 新增查看导出表, 导入表, 可以在PE查看器目录表里查看  
    6. 新增一个驱动程序, 打开进程使用, 可以打开 0x10010 这个窗口所在的进程, 进程名为 csrss.exe  
    7.   
      
后续计划:  
    1. 发送消息支持输入常量, 支持模糊输入  
    2. 发送消息的消息支持打开消息查看器获取  
    3. 发送消息的参数支持发送结构  
    4. 查看窗口子信息做全, 各类常见组件都需要完成  
    5. 生成常用代码, 包括创建窗口/常用功能执行后生成对应代码  
    6. 把PE目录表所有的表都弄出来  
    7.   
以上功能不能保证在什么时候开始, 什么时候完成  
也不保证能一定完成, 有时间会慢慢更新  
还有劝各位催更的, 你知道我为了这个都花费了多少心血吗?  
你知道我为了更新一个功能要死掉多少头发吗?  
你知道为了调试驱动程序, 电脑蓝屏了多少次吗?  
你不知道, 你们什么都不知道, 像你们这种催更的情况, 得加钱!!  
  
      
  
2.3版做完以下两个功能后就发布  
1. 查看组件子项信息, 支持调用插件实现查看信息  
2. 生成创建窗口/其他代码, 支持调用插件实现生成代码  
  
2023-02-02目标 查看数据窗口需要一个超级编辑框来显示详细数据  
  
2023-xx-xx 2.3.xxxx  
修复:  
    1. 修复 调整窗口尺寸错误的问题  
    2. 修复窗口树内存泄漏的问题  
    3. 完善属性树型框下的提示信息, SetProp/WLong/CLong  
    4.   
新增:  
    1. 窗口失效前会读取失效前的数据, 并用红色文本显示  
    2.   
      
      
          
1. 调整窗口修改调整的模式  
    左键调整窗口右下角, Ctrl+左键调整左上角  
    右键调整窗口左下角, Ctrl+右键调整右上角  
    Shift键以上模式取反  
2. 移动窗口修改移动模式  
    左键按下从窗口正中间移动窗口  
    Ctrl + 左键 从窗口底部移动窗口  
    Shift + 左键 从窗口顶部移动窗口  
3. 左右两边区域可调整尺寸, 最大化单独使用一个尺寸  
4. 左下角属性列表右键菜单根据不同功能显示不同菜单  
5. 增加模块查找功能  
6. 窗口树窗口失效红色显示, 被隐藏窗口灰色显示  
7. 新增展开/收缩窗口树, Ctrl + 选中菜单, 收缩时不收缩选中项, 不按Ctrl会收缩选中项, 展开不受影响  
    Tab键切换展开状态, 已经展开就收缩, 收缩状态就展开  
    Shift+Tab相当于按下了-(减号键)  
    Ctrl + Tab 等于选择了 展开该窗口 菜单项  
    Ctrl+Shift+Tab, 等于选择了 收缩该窗口 菜单项  
8. 窗口树支持 Ctrl + F 进行搜索了, F3 继续搜索下一个结果, Shift + F3 搜索上一个结果, 按下 Ctrl 键则只精确搜索窗口句柄  
  
  
2021-11-07 模块已经枚举出来了, 需要处理Ctrl + F 搜索  
需要把发送消息做一下, 直接内置在窗口里, 不需要单独做成插件  
需要处理一下属性树型框的快捷键, 现在只处理了 Ctrl + F  
编译路径需要更改, 配置文件也需要更改, 统一放到一个目录下, 看看使用什么名字  
