---
title: TextBoxControl.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: 轻松管理 TextBoxControl 的文本 - 获取或设置其内容，以实现无缝的用户交互并增强应用程序的功能。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.ole/textboxcontrol/text/
---
## TextBoxControl.Text property

获取或设置控件的文本。

```csharp
public string Text { get; set; }
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

* class [TextBoxControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
