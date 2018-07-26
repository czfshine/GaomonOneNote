# Gaomon&OneNote

一套适用于OneNote的高漫数位板配置文件

# Usage

* 关闭`Gaomon Tablet` 

* 将本项目的`config_user.xml` 文件替换`Gaomon Tablet` 程序目录下的`config_user.xml`

* 启动`Gaomon Tablet` 

  > 注意,替换配置文件后不能再使用`Gaomon Tablet`  进行快捷键的修改



# 快捷键分布

* 笔上面的两个键分别为上下滚轮

* 硬快捷键

  左上角

| 橡皮擦小 | 手柄 |
| ------- | --- |
| 橡皮擦中 | 套索 |
| 比划橡皮擦 | 键入 |

* 软快捷键


| 编号 | 颜色 | 类型   |
| ---- | ---- | ------ |
| 1    |      |        |
| 2    | 黄   | 铅笔细 |
| 3    | 绿   | 铅笔细 |
| 4    | 蓝   | 铅笔细 |
| 5    | 红   | 铅笔细 |
| 6    | 黑   | 铅笔粗 |
| 7    | 黑   | 铅笔细 |
| 8    | 黄   | 荧光细 |
| 9    |      |        |
| 10   |      |        |
| 11   |      |        |
| 12   |      |        |
| 13   |      |        |
| 14   |      |        |
| 15   |      |        |
| 16   |      |        |

# 配置文件解析

* `<HNDevices>`  根元素下的各个子项分别代表不同型号的设备,我的设备类型为`OEM02_T174` 修改下面的子节点即可
* `hbtns` 节点表示硬快捷键,`sbtns` 节点是软快捷键, `pbtns` 是笔上面的快捷键
* 每个快捷键节点由一系列`ekeyXX` 子项组成,分别对应各个快捷键(XX从0开始)
* `bCtrl` ,`bAlt`,`bShift` 等表示是否按对应的控制键,`kbkeyXX` 是一系列按键的对应编码,按顺序模拟按键(文档最下面有编码表)

举个例子,OneNote小橡皮擦的快捷键是 Alt,D,E,S,对应的按键编码是  18,68,69,83,我们把它设置成编号0的硬快捷键,
可以把 `HNDevices\OEM02_T174\hbtns\ekey0\kbtn`  下的元素设置成

```xml
<bCtrl>0</bCtrl>
<bAlt>0</bAlt>
<bShift>0</bShift>
<bWin>0</bWin>
<kbkey0>18</kbkey0>
<kbkey1>68</kbkey1>
<kbkey2>69</kbkey2>
<kbkey3>83</kbkey3>
<kbkey4>0</kbkey4>
....
<kbkey15>0</kbkey15>
```

 

| 编码 |描述|
|----|----|
|1 | 鼠标左键 |
|2| 鼠标右键 |
|3| CANCEL 键 |
|4| 鼠标中键 |
|8| BACKSPACE 键 |
|9| TAB 键 |
|12| CLEAR 键 |
|13| ENTER 键 |
|16| SHIFT 键 |
|17| CTRL 键 |
|18| ALT 键 |
|19| PAUSE 键 |
|20| CAPS LOCK 键 |
|27| ESC 键 |
|32| SPACEBAR 键 |
|33| PAGE UP 键 |
|34| PAGE DOWN 键 |
|35| END 键 |
|36| HOME 键 |
|37| LEFT ARROW 键 |
|38| UP ARROW 键 |
|39| RIGHT ARROW 键 |
|40| DOWN ARROW 键 |
|41| SELECT 键 |
|42| PRINT SCREEN 键 |
|43| EXECUTE 键 |
|44| SNAPSHOT 键 |
|45| INSERT 键 |
|46| DELETE 键 |
|47| HELP 键 |
|144| NUM LOCK 键 |
|65| A 键 |
|66| B 键 |
|67| C 键 |
|68| D 键 |
|69| E 键 |
|70| F 键 |
|71| G 键 |
|72| H 键 |
|73| I 键 |
|74| J 键 |
|75| K 键 |
|76| L 键 |
|77| M 键 |
|78| N 键 |
|79| O 键 |
|80| P 键 |
|81| Q 键 |
|82| R 键 |
|83| S 键 |
|84| T 键 |
|85| U 键 |
|86| V 键 |
|87| W 键 |
|88| X 键 |
|89| Y 键 |
|90| Z 键 |
|48| 0 键 |
|49| 1 键 |
|50| 2 键 |
|51| 3 键 |
|52| 4 键 |
|53| 5 键 |
|54| 6 键 |
|55| 7 键 |
|56| 8 键 |
|57| 9 键 |
|96| 0 键 |
|97| 1 键 |
|98| 2 键 |
|99| 3 键 |
|100| 4 键 |
|101| 5 键 |
|102| 6 键 |
|103| 7 键 |
|104| 8 键 |
|105| 9 键 |
|106| MULTIPLICATION SIGN (*) 键 |
|107| PLUS SIGN (+) 键 |
|108| ENTER 键 |
|109| MINUS SIGN (–) 键 |
|110| DECIMAL POINT (.) 键 |
|111| DIVISION SIGN (/) 键 |
|112| F1 键 |
|113| F2 键 |
|114| F3 键 |
|115| F4 键 |
|116| F5 键 |
|117| F6 键 |
|118| F7 键 |
|119| F8 键 |
|120| F9 键 |
|121| F10 键 |
|122| F11 键 |
|123| F12 键 |
|124| F13 键 |
|125| F14 键 |
|126| F15 键 |
|127| F16 键 |