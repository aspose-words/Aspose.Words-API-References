---
title: CommandButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: 发现 CommandButtonControl 类型属性以轻松访问 Forms 2.0 控件类型，增强应用程序的功能和用户体验。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.ole/commandbuttoncontrol/type/
---
## CommandButtonControl.Type property

获取 Forms 2.0 控件的类型。

```csharp
public override Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CommandButtonControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
