---
title: CommandButtonControl Class
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Ole.CommandButtonControl 类，轻松创建运行宏的交互式按钮，增强用户对应用程序的参与度。
type: docs
weight: 1450
url: /zh/net/aspose.words.drawing.ole/commandbuttoncontrol/
---
## CommandButtonControl class

CommandButton 控件运行一个宏，当用户单击它时，该宏会执行某个操作。

```csharp
public class CommandButtonControl : Forms2OleControl
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CommandButtonControl](commandbuttoncontrol/)() | 初始化一个新的实例`CommandButtonControl`类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | 获取或设置控件的背景颜色。 默认值取决于控件的类型。 |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | 获取或设置控件的 Caption 属性。 默认值为空字符串。 |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | 获取直接子控件的集合。 |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | 返回`真的`如果控制处于启用状态。 |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | 获取或设置控件的前景色。 默认值取决于控件的类型。 |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | 获取或设置指定一组互斥控件的字符串。 默认值为空字符串。 |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | 获取或设置控件的高度（以点为单位）。 |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | 返回`真的`如果控件是[`Forms2OleControl`](../forms2olecontrol/). |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | 获取或设置 ActiveX 控件的名称。 |
| override [Type](../../aspose.words.drawing.ole/commandbuttoncontrol/type/) { get; } | 获取 Forms 2.0 控件的类型。 |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | 获取通常代表控制状态的底层 Value 属性。 例如，选中的选项按钮的值为“1”，而未选中的选项按钮的值为“0”。 默认值为空字符串。 |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | 获取或设置控件的宽度（以点为单位）。 |

## 例子

展示如何插入 ActiveX 控件。

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### 也可以看看

* class [Forms2OleControl](../forms2olecontrol/)
* 命名空间 [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../)
