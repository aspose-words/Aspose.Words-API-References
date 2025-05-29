---
title: OleControl.IsForms2OleControl
linktitle: IsForms2OleControl
articleTitle: IsForms2OleControl
second_title: Aspose.Words for .NET
description: 探索 OleControl 的 IsForms2OleControl 属性，它可以识别您的控件是否为 Forms2OleControl，从而提高您的开发效率。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.ole/olecontrol/isforms2olecontrol/
---
## OleControl.IsForms2OleControl property

返回`真的`如果控件是[`Forms2OleControl`](../../forms2olecontrol/).

```csharp
public bool IsForms2OleControl { get; }
```

## 例子

展示如何验证 ActiveX 控件的属性。

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.AreEqual("First", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // 请注意，您不能为 Frame 设置 GroupName。
    checkBox.GroupName = "Aspose group name";
}
```

### 也可以看看

* class [OleControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
