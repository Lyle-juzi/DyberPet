<h1 align="center">
  呆啵宠物  |  DyberPet
</h1>

<p align="center">
  呆啵宠物 (DyberPet) 是一个基于 PySide6 的桌面宠物开发框架，致力于为开发者提供创造桌面宠物的底层软件
</p>

<p align="center">
  <a>
    <img src="https://img.shields.io/github/license/ChaozhongLiu/DyberPet.svg">
  </a>

  <a style="text-decoration:none">
    <img src="https://img.shields.io/github/downloads/ChaozhongLiu/DyberPet/total.svg"/>
  </a>

  <a style="text-decoration:none">
    <img src="https://img.shields.io/badge/python-3.9+-blue.svg" />
  </a>

  <a style="text-decoration:none">
    <img src="https://img.shields.io/badge/DyberPet-v0.5.3-green.svg"/>
  </a>
</p>

<p align="center">
简体中文 | <a href="README_EN.md">English</a>
</p>

![Interface](https://raw.githubusercontent.com/ChaozhongLiu/DyberPet/main/docs/DyberPet.png)

  
:octocat: 目前项目已在比较稳定的阶段，但仍然有很多功能在计划中。如果你有意向加入，请[私信我](https://space.bilibili.com/39307302)、或者直接 PR。欢迎一起构建框架 🥰 
  
（近期暂无大功能更新计划，会抽空修复 Bug 和清理代码。）
  
如果你喜欢这个桌宠程序，请点击右上角的 ⭐ **STAR**，这对我们有很大的激励！
  
:new: **08-22-2024: v0.5.1** 程序已打包上传 [Release](https://github.com/ChaozhongLiu/DyberPet/releases/tag/v0.5.1)，有任何问题欢迎向我反馈！  
  
:new: **06-26-2024**: CSDN 正大规模从 GitHub 搬运开源项目至其旗下 GitCode，包括 DyberPet。该仓库与我们没有任何关系。GitCode 使用我名字的主页也并非我本人创建，也请仔细甄别您在 GitCode 上看到的其他项目！
  
:new: **04-06-2024: v0.3.7** 已适配至 PySide6-Fluent-Widgets v1.5.4。 如果你在使用 Terminal 运行本程序，请用 pip 更新 PySide6-Fluent-Widgets。  
  
  
## 快速体验 Demo
### Windows 用户
  将 Release 下载至本地，双击 **``run_DyberPet.exe``** 即可


### Windows Terminal
  建议首先在本地创建新的 **conda** 环境  
  ```
  conda create --name Dyber_pyside python=3.9.18
  conda activate Dyber_pyside
  conda install -c conda-forge apscheduler
  conda install -c conda-forge pynput
  pip install PySide6-Fluent-Widgets==1.5.4 -i https://pypi.org/simple/
  pip install pyside6==6.5.2
  pip install tendo
  ```
  将仓库下载至本地，之后运行 **``run_DyberPet.py``** 即可

  
### MacOS 用户
  建议首先在本地创建新的 **conda** 环境  
  ```
  conda create --name Dyber_pyside python=3.9.18
  conda activate Dyber_pyside
  conda install -c conda-forge apscheduler
  pip install pynput==1.7.6
  pip install PySide6-Fluent-Widgets==1.5.4 -i https://pypi.org/simple/
  pip install pyside6==6.5.2
  pip install tendo
  ```
  将仓库下载至本地，之后运行 **``run_DyberPet.py``** 即可
  

## 素材与模组合集 

[这里](docs/collection.md)收录了现在已有的角色、物品模组、和迷你宠物，其介绍及下载链接。  
欢迎下载并通过 App 导入！
  
  

## 用户手册
请参考用户手册，体验现有功能 (施工中)




## 开发者文档
### 素材开发
若您想要在现有功能下，开发一套新的宠物形象、动作，请参考[素材开发文档](docs/art_dev.md)

### 功能开发
若您想要在现有模块下，开发新的功能，请参考[功能开发文档](README.md) (施工中)


## 更新日志

<details>
  <summary>版本更新列表</summary>
  
**v0.5.4 - 09/01/2024**
- 优化了迷你宠物仅在 X 轴跟随角色时的行为（左右行走、被拖拽开后自动回到角色身边）
- 修复了迷你宠物中当 anchor 与 缩放因子相乘后不为整数导致的上下漂移问题
- 主宠物动画模块同上
- 切换宠物时，强制将角色移动到正确的位置，以避免 Qt 内部错误导致的位移

**v0.5.3 - 08/31/2024**
- 在系统设置中添加了关闭弹出通知栏的功能
- 取消了一次只能召唤一个迷你宠物的限制

**v0.5.2 - 08/25/2024**
- 初始化数据时会清除负数物品
- 单击角色时浮动的心心由随机位置更改为了点击位置

**v0.5.1 - 08/22/2024**
- 添加了日期更新 Timer
- 日期更新时自动更新喂养的天数
- 修复了不满足饱食度要求的动作附加声音被播放的错误

**v0.5.0 - 08/16/2024**
- 在左键拖拽情况下锁定右键菜单
- 修复了右键点击 Event 的错误代码 (虽然不影响使用)

**v0.5.0 - 08/14/2024**
- 改进了和游戏存档相关的各项功能，避免因存档文件问题导致的崩溃和闪退
- 替换了右键菜单的更换角色图标

**v0.5.0 - 08/10/2024**
- 修复了当迷你宠物跟随主宠物时，因目标坐标设定低于水平线导致的抽搐现象

**v0.5.0 - 08/06/2024**
- 移除了物品掉落组件我自己画的难看的气泡
- 检查新添加角色模组时，patpat 不再是必须属性
- 修复了导入新角色后，以同伴组件进行召唤，因缺少数据初始化而导致程序崩溃的问题

**v0.5.0 - 08/05/2024**
- settings 添加了 ``minipet_scale`` 来独立设定迷你宠物的大小
- 迷你宠物菜单中添加了大小调节 Slider
- 修复了召唤同伴或迷你宠物拍拍动作的调用错误

**v0.5.0 - 08/03/2024**
- 细化了 ``宠物大小`` 设置参数，现在每一个角色都有独立的大小参数
  
**v0.5.0 - 07/21/2024**
- 修复了在商店卖出物品的最后一个时，背包内仍然显示该物品的 Bug

**v0.4.9 - 07/15/2024**
- 修复了取消专注时间再次开始后程序崩溃的 Bug
- 初始化的动作会被自动勾选加入播放列表
- 修复了部分 UI 显示不全的问题
- 优化了对话框的出现位置
- 修复了宠物默认动作存在 Anchor 时的正确初始位置

**v0.4.8 - 06/29/2024**
- 统一参数 ``set_fall`` 为 Boolean，并添加进了 settings.json 文件中

**v0.4.7 - 06/15/2024**
- 修复了系统界面一些对话框选项错误的问题
- 修复了缺少的语言类型的初始化问题
- 添加了软件更新提醒通知
- 添加了对应更新的翻译

**v0.4.6 - 05/11/2024**
- ``pet_conf.patpat`` 类型更换为 ``dict {0:"actname", 3:"actname2"}``, 可以给每个饱食度等级单独定义拍拍动画
- 更新了交互模块拍拍动画的播放逻辑，会首先按当前饱食度等级随机选取一个拍拍动画

**v0.4.5 - 05/10/2024**
- 重构了所有的数值条，解决了之前数值过小时 Bar 超出圆角边界的问题

**v0.4.4 - 05/07/2024**
- 添加了迷你宠物管理 UI 和功能
- 之前的 ``附属宠物/subpet`` 正式更名为 ``迷你宠物``
- 更新了系统面板的部分 UI

**v0.4.3 - 05/05/2024**
- 在基本设置中 添加了自定义应用主题色功能
- 在基本设置中 添加了检查更新的功能

**v0.4.2 - 05/04/2024**
- 简化了右键菜单结构
- 给宠物拖拽添加了反弹机制

**v0.4.2 - 05/03/2024**
- 添加了 ``自定义动作`` 和 ``动作设计`` 功能
- 完善了动画面板的功能和 UI
- 添加了动画面板相关的翻译
  
**v0.4.1 - 04/20/2024**
- ``ActData`` 添加了 ``special_act`` 属性
- 如果你曾在 04/18 - 04/20 之间测试使用过新的终端版本程序，或许需要删除 ``data/act_data.json`` 重新生成

**v0.4.1 - 04/18/2024**
- 在新的``ActData``基础上
  - 更新了交互模块、附件模块的逻辑
- 给 ``act``、``acc``、``anchor`` 添加了``跳过``的配置数值
  - 各模块判定为跳过动画是会按设定的逻辑执行
  - 动画模块&交互模块：按跳过的配置 图像静止不动
  - 附件模块：遇到跳过会暂时隐藏，直至下一个附件动画出现
- 下一步会开发动作模块 UI，用来自定义动作

**v0.4.0 - 04/14/2024**
- 重构了动画模块的配置数据结构 ``ActData``
- 在新的数据结构基础上
  - 更新了动画模块的逻辑
  - 更新了动画选择菜单的功能逻辑
  - ！交互模块仍未更新，可能会触发问题

**v0.3.7 - 04/09/2024**
- 给角色面板添加了更多的指南
- 角色如果包含 ``items`` 文件夹，会自动判定并导入其中的物品

**v0.3.7 - 04/06/2024**
- 通知栏剩余翻译完成
- 采用 Fluent-Widgets 优化了通知栏 UI
- 优化了缩放逻辑以避免在 MacOS 中的地面判断 bug
- 适配到了 Fluent-Widgets 1.5.4 版本；请尝试使用 pip 更新环境中的 PySide6-Fluent-Widgets

**v0.3.7 - 03/31/2024**
- 代办事项 UI 和功能完成
- 角色面板的翻译全部完成

**v0.3.6 - 03/15/2024**
- 每日进度功能代码更新
- 存档数据新增了 ``task_data.json``
  - 存档导出、快速存储时会被备份，但不会被导入
  - ``conf.py`` 中增加了 ``TaskData`` 的各种操作
  - App 启动时加载 ``settings.task_data``

**v0.3.6 - 03/05/2024**
- 专注任务功能代码基本完成
- 优化了番茄钟和专注时间倒计时UI的显示区域及其对主动画模块的影响

**v0.3.5 - 02/18/2024**
- 日常任务 UI 设计完毕
- 日常目标 UI init

**v0.3.5 - 02/04/2024**
- 日常任务 UI init

**v0.3.5 - 01/21/2024**
- 动作管理 UI init
- 将程序中几乎所有的 ``QImage`` 替换成了 ``QPixmap``，以节省内存，优化运行效率

**v0.3.4 - 01/21/2024**
- 商店购买和出售功能实装

**v0.3.4 - 01/18/2024**
- 商店 UI 同步角色属性进行刷新
  - 物品增减
  - 角色好感度变化
  - 切换角色
  - 导入存档
- 物品默认价格按星级提升

**v0.3.4 - 01/16/2024**
- 商店 UI 代码完成
  - 界面设计和代码完成
  - 实装了按字符搜索
  - 实装了按标签筛选
- 商店各项功能暂未完成

**v0.3.4 - 12/26/2023**
- 高分辨率屏幕图片缩放优化
- Avatar Label 生成方法优化
- 将默认未知 Icon 换成了空白图片

**v0.3.4 - 12/13/2023**
- BUFF系统 init
  - 物品（包括宠物）添加了 ``buff`` 属性，详见 [buffModule](DyberPet/Dashboard/buffModule.py)
  - 状态面板添加了 Buff 的运算和 UI，仍在施工中
- 薯条、汉堡、派蒙均添加了 ``buff`` 属性作为demo的例子
- ``HP`` 下降timer缩短为1分钟

**v0.3.3 - 11/28/2023**
- 宠物系统 init
  - 宠物是每个角色的宠物（宠物的宠物 hhh），作为Item Class，可被获取
  - 宠物可跟随角色，或自由活动
  - 宠物可对角色有Buff加成（未完成）
- 添加了 ``派蒙`` 作为一个宠物的例子
- **声明**：从v0.3.3起，桌宠将用``角色``指代，桌宠的宠物用``宠物``指代

**v0.3.2 - 11/24/2023**
- 背包面板刷新机制
- 金币系统 init

**v0.3.2 - 11/21/2023**
- 背包面板基本完成
- 背包空白格背景颜色更改
- 切换宠物时的刷新还未完成
- 删除了旧的背包UI
- 进行了少量的代码清理

**v0.3.2 - 11/16/2023**
- 背包面板 init
  
**v0.3.2 - 11/12/2023**
- 状态信息构建完成
- 角色面板构建完成

**v0.3.1b - 11/10/2023**
- 角色面板 init
- 状态信息日志 Widget init

**v0.3.1b - 11/05/2023**
- 修复了设置界面圆角显示不全的问题
- 优化了菜单 UI 子菜单点击的行为逻辑
- 修复了屏幕缩放导致部分组件重叠的问题
- MacOS 的兼容性改进
  - 修复附件模块无法正常显示的问题
  - 修复“前往文件夹”无法运行的问题
  - 优化窗口大小计算，但Mac仍然存在屏幕大小获取问题
  
**v0.3.1b - 10/27/2023**
- 切换了打包方式
  
**v0.3.1 - 10/21/2023**
- 切换至了 PySide6-Fluent-Widgets 1.3.3
- 修复了一些上报和未上报的潜在bug
- 补充了一些缺失的翻译
- 近期更新的本地测试完成
- release 添加 PySide6 版本


**v0.3.0a - 10/21/2023**
- 完成了物品模组功能
- 完成了物品模组的翻译


**v0.3.0a - 10/17/2023**
- 框架 main 分支迁移至 PySide6

    
**v0.3.0a - 10/08/2023**
- 框架迁移至 PySide6
- 添加了物品模组功能（未完成）

**v0.3.0a - 09/24/2023**
- 添加了系统及 UI
  - 基本设置 UI：替换了原本的设置，更贴近 Windows11；增加了语言切换设置
  - 存档管理 UI：实装了存档系统，包括存档的导出、导入，快速存档功能
  - 角色管理 UI：显示角色列表，包含启动按钮、角色信息卡片
- 存档系统改动
  - 存档改动为每个角色独立
  - 添加了新旧存档的自动转换代码
  - 添加了存档文件的各种操作（详见 [添加了系统及 UI]）
- 语言切换
  - 完成了语言切换功能
  - 新增了语言切换相关的文件：``langs.pro``, ``res/language``
  - 部分完成了中英两种语言的翻译
- 重构了原有 UI
  - 利用 PyQt5 原生功能重新实现 按分辨率和缩放改变大小
  - 优化了菜单 UI，替换为 PyQt-Fluent-Widgets RoundMenu
  - 将状态栏移动到了右键菜单中
  - 开启计划任务时，进度条会持续出现在宠物上方
  - 替换了通知窗口的关闭按钮
- 角色添加功能
  - 角色管理UI基本完成
  - 实现了角色添加的基本功能

  
**v0.2.2 - 03/14/2023**
- 数据存写大概花费0.43ms，有极小概率在该间隔内关闭软件导致数据丢失。本次优化在每次关闭前主动存储一次数据，并冻结数据，执行退出。
  
**v0.2.2 - 03/09/2023**
- 可以客制化番茄钟了
- 修复了狂爆物品的另一个大bug
  
**v0.2.2 - 03/08/2023**
- Mac不兼容通知栏关闭按钮，故优化了关闭按钮UI
  
**v0.2.2 - 03/07/2023**
- 附件动作的``follow_mouse``属性添加了``"x"`` 和 ``"y"``的选项，可单独跟随x或y轴
  
**v0.2.2 - 03/05/2023**
- 常驻动作数据结构修改，bug修复
- 同伴添加了常驻动作判定，需要在是主宠物时进行设定
  
**v0.2.2 - 03/04/2023**
- 添加了下落的前置动作``prefall``，将在鼠标松开后执行
- 背包分成了食物和收藏品两栏
  
**v0.2.2 - 03/03/2023**
- 右键菜单中增加了常驻动作选项，可以改变闲置时的默认动作，选中后将不在随机播放其他动作
  
**v0.2.2 - 03/02/2023**
- 交互功能添加了水平跟随目标的功能
- 添加了跟随鼠标的功能
- 目标跟随需要在``pet_conf.json``中定义``left``向左移动和 ``right``向右移动的动作
  
**v0.2.2 - 03/01/2023**
- 存档系统初步功能上线
  
**v0.2.1 - 02/25/2023**
- ``fv_reward``属性可设置为list，物品可出现在多个等级奖励中
  
**v0.2.1 - 02/23/2023**
- Windows系统添加了subwindow属性
- 禁用掉落时，缩放宠物不会闪回地面
  
**v0.2.1 - 02/22/2023**
- 优化了缩放机制
- 物品数量为1时不显示数字
- 优化了主宠物列表判断和默认宠物的保存方式
  
**v0.2.0 - 02/21/2023**
- MacOS 兼容性代码改进
- 增加好感度等级奖励的补偿系统
  
**v0.2.0 - 02/18/2023**
- 设置中添加了启动默认角色的选择
- 切换角色增加了问候通知
- 添加了 NoDropShadowWindowHint （为MacOS准备）
  
**v0.1.19 - 02/16/2023**
- 设置中可以静音了
- 添加了统计陪伴天数及显示铭牌的功能
  
**v0.1.18 - 02/12/2023**
- 对话框自动添加上一步按钮
- 调整了对特殊中文字符的长度计算
  
**v0.1.18 - 02/11/2023**
- 增加了附属宠物和主宠物的连接
- 保证收藏品在随机掉落中不重复出现
- 整理了可变更的系统数值
  
**v0.1.18 - 02/10/2023**
- 添加了对话界面和功能（暂未实装素材）
  
**v0.1.17 - 02/05/2023**
- 给通知系统语音添加了优先级``sound_priority``属性
- 增加了点击时的随机语音事件
- 增加了纳西妲的语音库
  
**v0.1.16 - 02/01/2023**
- 实现了多屏之间转移（测试中）
- 规避了专注时间0分0秒相关的闪退bug
- 解决了不能言说的狂爆物品惊天大bug
- 停止按钮按下后会立刻失效，避免多次结算
- 修复了快速点击鼠标微小位移造成闪现的bug
- 修复了召唤同伴放大时显示不全的问题
- 修复了一定条件下缩放宠物派蒙位置问题
  
**v0.1.15 - 01/29/2023**
- 取消屏幕缩放对图片大小的影响
- 重力加速度最小值变为0.01
- 数值栏字体固定为Times
- 设置内添加是否置顶的选项
  
**v0.1.14 - 01/28/2023**
- 修复了禁用掉落时不会触发摸摸事件的bug
- ``pets.json``转移到了``res/role/``
  
**v0.1.14 - 01/23/2023**
- ``item_config``更新
  - 添加了``fv_reward``: int，将物品设定为好感度升级奖励
  - 修复了label anchor未随缩放比例改变的bug
  - 重力加速度最小值变为0.01
  - 取消屏幕缩放比例对图片大小的影响
  
**v0.1.14 - 01/22/2023**
- ``pet_config['acc_act']``更新
  - ``timeout``：true/false 动画结束后关闭 / 不断循环
  - ``unique``：true/false 可否存在多个一样的附件
  - ``closable``：true/false 可否关闭（右键菜单关闭）
  - ``follow_main``：true/false 是否跟随主程序移动
  - ``speed_follow_main``：int 跟随主程序的移动速度
  
**v0.1.13 - 01/21/2023**
- 优化了widget size的动态变化逻辑
- 修复了没有随机动作或随机动作概率为零时的报错
- 通知栏边框变为圆弧
- 饱食度下降间隔变为 2min
- ``pet_config`` 更新
  - 添加了``subpet``，用来定义宠物的附属宠物
  - ``item_favorite``, ``item_dislike`` 变更为``dict``, 增加了物品好感度倍率数值
- ``item_config``更新
  - 添加了``type``, 可添加消耗品``consumable``和收藏品``collection``两类物品，收藏品不可使用
- ``act_config``更新
  - 添加了``anchor``属性，将根据锚点自动移动动画
- 开始施工语言更换
  
**v0.1.12 - 01/15/2023**
- 待机动作（default）将持续进行
- 更改了数值模块的逻辑，目前所有宠物共用一套数值
  - 删除了``pet_config``中的 ``gravity``, ``hp_interval``, ``fv_interval``
- 进程多开被禁止，以防数据存储混乱
- 多开禁止的情况下，为了能够让多个宠物同屏，增加了``召唤同伴``的功能
- 增加了鼠标点击触发的``摸摸事件``，宠物可定义摸摸的动作，并大概率触发向上浮动的心心，小概率获得物品掉落
- 增加了物品掉落的动画，掉落物品呈抛物线掉落在底部任务栏

**v0.1.11 - 01/07/2023**
- 添加了设置界面，可以改变大小、重力、拖拽速度、音量
- 添加了组件动作：现在支持动作包含另一个动画的功能（具体见素材开发文档）
- 物品使用添加了宠物喜爱度的分级，可设置不同的声音、动作
- 支持宠物自定义通知图标和声音，在``res/role/NAME/note/`` 中添加 （具体见素材开发文档）
- 宠物移动行为增加了屏幕边界
  
**v0.1.10 - 12/28/2022**
- 通知栏的图标和声音与 note_type 关联，可在 ``res/role/PETNAME/note/note_config.json`` 中自定义
  
**v0.1.10 - 12/27/2022**
- 更新了提醒事项的 UI
- 更新了饱食度随时间下降的计算逻辑，每一分钟都会变化，但只显示百分比，与用户定义的 ``hp_interval`` 相关
  
**v0.1.9 - 12/25/2022**
- 更新了番茄钟和专注时间的 UI
- 番茄钟和专注时间的开始和取消移动到了各自的界面内，不再使用菜单进行
- 专注时间可以暂停了
- 专注时间取消也会按已经行的时长获取物品奖励
  
**v0.1.8 - 12/21/2022**
- 界面大小加入了屏幕缩放比例的考虑
- UI 仍然没有全部完成
- 加入了圣诞限定小猫角色
  
**v0.1.8 - 12/19/2022**
- 交互模块QTimer变为更加精准的Timer
  
**v0.1.8 - 12/18/2022**
- 数值系统更新：健康值和心情值替换为 饱食度、好感度，并更新了数值系统及其 UI
- 增加了更多模块连接
  - 数值改变将影响随即动作的触发几率、每个动作的具体概率
  - 动作和物品将伴随好感度提升解锁
  - 更多细节将在用户手册和素材开发文档中更新
- 下落动作细分为 下落中 + 落地动作 两个部分
- 更新了背包系统的 UI，后续将逐渐更新所有的 UI 界面
  
**v0.1.7 - 12/11/2022**
- 添加了计划任务完成后的物品掉落事件

**v0.1.7 - 12/10/2022**
- 添加了背包系统，可以使用宠物获得的物品（目前只是功能测试阶段，UI极其丑陋，甚至不一致）
  - 在 settings 中增加了 pet_data，用来存储宠物数值和物品的数据
  - 添加了 item_data 和 ``res/items/item_config.json``，用于素材开发中设定物品属性（素材开发文档待更新）
  - 完善了背包交互的一系列可能行为的系统反馈，尽可能考虑了各种情况（可能仍然有bug）
  - 连接了物品使用与数值变化、动画播放
- 添加了通知系统，将取代旧版本中的对话框
  - 定义了 QToaster class 及目前定义的通知类型字段
  - 通知消息会伴随喵叫声
  - 为物品使用和数值变化添加了通知
  - 为计划任务添加了通知，删除了对话框显示（代码仍然在）

**v0.1.6 - 12/03/2022**
- 添加了提醒事项的到时提醒
- 添加了间隔提醒功能
- 关闭宠物后，备忘录会保留
- 添加了对话显示的排队系统，避免冲突

**v0.1.6 - 12/02/2022**
- 添加了专注时间功能
- 添加了番茄时钟和专注时间的倒计时
- 添加了提醒事项（备忘录）
- 该版本下，健康和心情会不断下降，暂时没有和其他功能连接，会在后续版本中添加

**v0.1.5 - 11/27/2022**
- 解决了使用 ``apscheduler`` 时 ``pyinstaller`` 的 bug
- 添加了番茄时间功能

**v0.1.5 - 11/26/2022**
- 采用 ``apscheduler`` 规范化了计划任务模块
- 增加了宠物数值相关数据的读取、修改、存储系统
- 重构了文件夹结构

**v0.1.5 - 11/25/2022**
- 增加了对话框和显示对话的功能
- 增加了计划任务模块
- 计划任务模块增加任务：运行时打招呼、健康和心情随时间下降

**v0.1.4 - 11/23/2022**
- 增加了心情数值
- 更新了呆啵宠物的图标

**v0.1.4 - 11/20/2022**
- 增加了鼠标停留时数值系统的显示 （未实装功能）

**v0.1.3 - 11/19/2022**
- 模块化重构了项目代码

**v0.1.2 - 11/14/2022**
- 最初版本上线


</details>

## 致谢
- UI 重构基于 [Fluent-Widgets](https://github.com/zhiyiYo/PyQt-Fluent-Widgets)，感谢作者 [zhiyiYo](https://github.com/zhiyiYo) 的指导和帮助
- Demo 中的部分素材来自 [daywa1kr](https://github.com/daywa1kr/Desktop-Cat)
- 框架早期的动画模块的逻辑参考了 [yanji255](https://toscode.gitee.com/yanji255/desktop_pet/)  
- 框架拖拽掉落的计算逻辑参考了 [WolfChen1996](https://github.com/WolfChen1996/DesktopPet)
