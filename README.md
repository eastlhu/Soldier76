<!-- # Soldier76 ![76_logo](./static/img/76_logo.png) -->

<!-- PUBG - G502鼠标宏自动压枪脚本使用说明 -->

<!-- ***(务必...务必...务必...认真看完，使用说明写的很详细了)*** -->

<h1 align="center">
  Soldier76 <img src="./static/img/76_logo.png" alt="76_logo">
</h1>
<div align="center">PUBG - Logitech鼠标宏自动压枪脚本使用说明</div>
<div align="center"><i><b>(务必...务必...务必...认真看完，使用说明写的很详细了)</b></i></div>
<div align="center"><s>Ps: 如果认为游戏体验有提升的话，请给我一颗小星星:)</s></div>
<br>
<p align="center">
  <img src="https://img.shields.io/badge/lua-5.1-00007F.svg" alt="lua-5.1">
  <img src="https://img.shields.io/badge/logitech-✔-A7F079.svg" alt="logitech-✔">
  <img src="https://img.shields.io/badge/lgs-9.02.65-00B8FC.svg" alt="lgs-9.02.65">
  <img src="https://img.shields.io/badge/version-3.x-29D1E3.svg" alt="version-3.x">
</p>
<!-- ![lua-5.1](https://img.shields.io/badge/lua-5.1-00007F.svg) ![version-3.x](https://img.shields.io/badge/version-3.x-56B6C2.svg) ![g502-✔](https://img.shields.io/badge/g502-✔-98C379.svg) ![gpw-✖](https://img.shields.io/badge/gpw-✖-E06C75.svg) -->

---

### 下载脚本
* 选择<a href="https://github.com/kiccer/Soldier76/releases" target="_blank">下载</a>版本
* 版本号**a.b.c**由三个部分组成
* **a**是大版本号，此版本号改动时，将可能会造成操作方式上的改变
* **b**是次版本号，通常表示有新功能上线
* **c**是修订号，通常表示修复了BUG，或是正在测试新的功能，不一定稳定
* 下载时请尽量选择**a.b**形式的版本号，例如**v3.3**，这种是经过测试相对比较稳定的版本

### 安装教程
1. **以管理员身份**启动罗技驱动
2. 扫描游戏
3. 开启 **自动游戏检测**
4. 右键配置文件右侧 **PUBG** 图标 -> **编写脚本**
5. 将 **Soldier76.lua** 中包含的所有代码完全复制进去，保存(Ctrl + S)
6. 右键 **PUBG配置** 和 **默认配置** 中的 **G6**, **G7**, **G8**, **G9**, **G10**, **G11** 按钮 -> **取消分配**

### 游戏设置
* 将**开镜**设置为**按住右键**，**必需设置** (注意，这里说的是**按住**，不是单击)
* 如果使用腰射压枪功能，需要把腰射键改为**左ctrl**键，可选，推荐
* 如果使用自动连发功能，需要把开火键改为键盘按键（例如：~键），可选，不推荐

### G键功能(默认设置)
G键 | 功能
:--: | ---
**G6** | 切换至 **5.56** 枪械配置文件表，并使用**第一个**配置
**G7** | 切换至 **9mm** 枪械配置文件表，并使用**第一个**配置
**G8** | 切换至 **7.62** 枪械配置文件表，并使用**第一个**配置
**G9** | 切换至 **.45** 枪械配置文件表，并使用**第一个**配置
**G10** | 切换至**最后一个**配置 (滚轮右偏)
**G11** | 切换至**下一个**配置 (滚轮左偏)

### 什么是切换？
> 很多人没搞清楚切换是什么意思，这是我们脚本与众不同的地方。
>
> 这个脚本中有一个枪械库，枪械库根据子弹类型分成不同系列，包括： **.45** 系列、 **9mm** 系列、 **5.56** 系列和 **7.62** 系列。每个系列下存放着匹配弹药类型的枪械，比如5.56系列下的第一把枪就是 **M416** 。 **G6-G9** 一共4个键，每个键即代表一个系列，单击后将切换至对应系列的枪械表，并且自动选中列表中的第一把枪。多次按G11键可以向下选择枪支，如果你需要的是该系列中的最后一把枪，只需按一次G10即可。
>
> 举个例子：你捡到了一把 **AKM** ，你只需要点击一下 **G8** 键，就可以了，因为 **AKM** 就是 **7.62** 系列中的第一把枪。如果你又捡到了一把 **QBZ** ，你不要你的 **AKM** 了，这时你需要先点击一次 **G6** ，切换到 **5.56** 系列时默认选中了第一把枪，而 **QBZ** 是第三个，所以你还要再按2次 **G11** ，这样你才能使用 **QBZ** 的数据。
>
> 枪械顺序请查看源代码中的 `userInfo.canUse`，排列顺序即枪械顺序。
>
> 以上G键功能都可以自定义设置，默认为g502设置，其他logitech系列可编程鼠标也全都支持。如果自己不会设置和调整，欢迎加群向我们询问。

### 指令列表
指令 | 功能
:--: | ---
**.45** | 切换至 **5.56** 系列枪械列表，并使用该列表下的第一把枪
**9mm** | 切换至 **9mm** 系列枪械列表，并使用该列表下的第一把枪
**5.56** | 切换至 **5.56** 系列枪械列表，并使用该列表下的第一把枪
**7.62** | 切换至 **7.62** 系列枪械列表，并使用该列表下的第一把枪
**first** | 切换至当前列表的第一把枪
**next** | 切换至当前列表的下一把枪
**last** | 切换至当前列表的最后一把枪

### 模式控制
按键 | 功能
:--: | ---
**CapsLock** | 开启大写字母键，启动宏，关闭则锁定宏(宏将暂时不可用，但配置记录保留)
**ScrollLock** | 开启开发者调试模式，准星自动向右拉(开启后尝试修改 `InGameSightingSensitivity` 的值，使弹道变成一字)

### 瞄准设置
参数 | 描述
:--: | ---
**default** | 使用游戏初始默认的设置，即点击右键开镜，长按右键瞄准。(单纯点击操作时需要按住左shift)
**recommend** | 使用此脚本推荐设置，即长按右键开镜，长按左ctrl瞄准。
**custom** | 自定义设置，使用在 `pubg.isAimingState` 方法的自定义区域中设置的判断条件。

### 使用方法
* 在右键(按住开镜)按住的情况下，点击左键启动压枪宏
* 在左Ctrl键(腰射)按住的情况下，点击左键启动压枪宏
* 开镜并按住左Alt键的情况下，点击左键启动4倍压枪宏
* 按住shift屏息时，将会暂停自动压枪功能

### 初次使用
1. 按照 [#安装教程](https://github.com/kiccer/Soldier76#%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B) 安装脚本
2. 然后再更改游戏内设置，参考 [#游戏设置](https://github.com/kiccer/Soldier76#%E6%B8%B8%E6%88%8F%E8%AE%BE%E7%BD%AE)
3. 修改脚本 `userInfo.canUse` 中的枪械，设置 `UMP45` 为 **1**，其他全部设置为 **0**。(**自动游戏检测时，切换窗口会导致脚本重启，因此不会记录上一次配置表的位置信息，将可用枪械限制为1个有利于调试，你也可以选择保留其他的枪**)
4. 进入训练场，按照注释提示，给枪支安装指定配件。
5. 开启 `CapsLock` 和 `ScrollLock`，面对墙壁，按住右键开镜，按住左键开火，你会发现准星自动往右偏移，请不要移动鼠标，直到子弹打光。
6. 如果弹印不是一条水平线，则修改 `userInfo.InGameSightingSensitivity` 的数值，上下微调即可。
7. 回到游戏感受弹道变化，重复以上修改操作，继续尝试，直到弹道变成一条水平线为止。
8. 如果数值无论怎么修改都无法变成一条水平线，请尝试略微调整游戏内的鼠标灵敏度。
9. 当弹道成功打成一条水平线时，关闭 `ScrollLock`，然后再次对着墙壁进行射击。如果没有意外，那么恭喜你，你的宏已经能够准确的自动压枪了！
10. 修改脚本 `userInfo.canUse` 中的枪械，将你需要的枪械设置为 **1**
11. `ctrl+s` 保存脚本后，可以在编辑器里尝试切换配置，切换配置时会有对应的文本信息输出，你可以在这里确认是否和心里预期的配置信息相同。
12. 最后一步，寻找队友，然后尽情装逼吧~

### 硬件条件
* 一只可编程 Logitech 鼠标
* 游戏画面不卡顿，不频繁掉帧，必要时可以锁定帧数保证稳定性

### 免责声明
* **该脚本程序仅供学习交流，严禁使用于任何商业用途，若产生利益纠纷，概不负责。**
* **请尊重作者的劳动成果，如需转载，请注明出处，谢谢！**
* **不可将此脚本二次创作后用于商业目的！**

### 交流群
* 欢迎加入技术交流QQ群：[![logitech 鼠标宏技术交流](./static/img/group.png)](https://kiccer.github.io/Soldier76/static/join_group.html)
* 十分欢迎愿意给本项目精调弹道的小伙伴
* 我们也同样欢迎其他项目的小伙伴入驻，一起交流技术话题

### 问题反馈
* 使用脚本时有任何疑问，或脚本存在不足之处可以在 [`issues`](https://github.com/kiccer/Soldier76/issues) 反馈给我

### 关于宏
* 宏就像是一个心灵手巧的瞎子
* 它可以帮你做更复杂细腻的操作
* 但无法根据实时情况进行变通
* 所以菜的人依旧菜得真实……

### Need help
My English is not very good, and the translation results of translation software are usually very strange. So I need a translator to help me translate this document into other languages. If you can, please contact me.

If you could directly `fork` the project and create a `README.[lang].md`, then `Pull Request` would be great for me.

<!-- ~~Ps: 如果认为游戏体验有提升的话，请给我一颗小星星:)~~ -->
