---
title: CommandButtonControl
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words for .NET
description: 探索 CommandButtonControl 构造函数。使用这个强大的类实例，轻松为您的应用程序创建和自定义按钮。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.ole/commandbuttoncontrol/commandbuttoncontrol/
---
## CommandButtonControl constructor

初始化一个新的实例[`CommandButtonControl`](../)类.

```csharp
public CommandButtonControl()
```

## 例子

展示如何插入 ActiveX 控件。

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### 也可以看看

* class [CommandButtonControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
