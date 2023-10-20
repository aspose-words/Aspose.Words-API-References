---
title: OleFormat.OleControl
linktitle: OleControl
articleTitle: OleControl
second_title: 用于 .NET 的 Aspose.Words
description: OleFormat OleControl 财产. 获取OleControl如果此 OLE 对象是 ActiveX 控件则为对象否则此属性为空 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

获取`OleControl`如果此 OLE 对象是 ActiveX 控件，则为对象。否则此属性为空。

```csharp
public OleControl OleControl { get; }
```

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

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
