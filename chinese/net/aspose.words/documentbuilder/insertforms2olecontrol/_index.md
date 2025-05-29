---
title: DocumentBuilder.InsertForms2OleControl
linktitle: InsertForms2OleControl
articleTitle: InsertForms2OleControl
second_title: Aspose.Words for .NET
description: 轻松将 Forms2OleControl 与 DocumentBuilder 的 InsertForms2OleControl 方法集成。立即增强您的文档功能！
type: docs
weight: 350
url: /zh/net/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder.InsertForms2OleControl method

插入[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/)对象进入当前位置。

```csharp
public Shape InsertForms2OleControl(Forms2OleControl forms2OleControl)
```

### 返回值

[`Shape`](../../../aspose.words.drawing/shape/)包含传递的对象[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/)

## 例子

展示如何插入 ActiveX 控件。

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### 也可以看看

* property [OleFormat](../../../aspose.words.drawing/shape/oleformat/)
* property [OleControl](../../../aspose.words.drawing/oleformat/olecontrol/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
