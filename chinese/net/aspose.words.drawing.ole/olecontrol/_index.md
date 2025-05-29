---
title: OleControl Class
linktitle: OleControl
articleTitle: OleControl
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Ole.OleControl 类，以便在您的应用程序中无缝集成 OLE ActiveX 控件，从而增强功能。
type: docs
weight: 1500
url: /zh/net/aspose.words.drawing.ole/olecontrol/
---
## OleControl class

表示 OLE ActiveX 控件。

要了解更多信息，请访问[使用 Ole 对象](https://docs.aspose.com/words/net/working-with-ole-objects/)文档文章。

```csharp
public class OleControl
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | 返回`真的`如果控件是[`Forms2OleControl`](../forms2olecontrol/). |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | 获取或设置 ActiveX 控件的名称。 |

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

* 命名空间 [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../)
