---
title: TextBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: 探索 Forms 2.0 的 TextBoxControl Type 属性，实现无缝控制定制并增强应用程序中的用户体验。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.ole/textboxcontrol/type/
---
## TextBoxControl.Type property

获取 Forms 2.0 控件的类型。

```csharp
public override Forms2OleControlType Type { get; }
```

## 例子

展示如何更改 TextBox OLE 控件的文本。

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### 也可以看看

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [TextBoxControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
