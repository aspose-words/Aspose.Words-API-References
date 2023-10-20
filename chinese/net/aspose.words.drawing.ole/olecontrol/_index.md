---
title: OleControl Class
linktitle: OleControl
articleTitle: OleControl
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.Ole.OleControl 班级. 表示 OLE ActiveX 控件 在 C#.
type: docs
weight: 1140
url: /zh/net/aspose.words.drawing.ole/olecontrol/
---
## OleControl class

表示 OLE ActiveX 控件。

```csharp
public class OleControl
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | 如果控件是[`Forms2OleControl`](../forms2olecontrol/). |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | 获取 ActiveX 控件的名称。 |

## 例子

演示如何验证 ActiveX 控件的属性。

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual(null, oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../)
