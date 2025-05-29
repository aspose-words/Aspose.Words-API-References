---
title: Forms2OleControl.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words for .NET
description: 了解如何轻松调整 Forms2OleControl 的 Width 属性，以点为单位精确调整控件大小。轻松提升您的 UI 设计！
type: docs
weight: 100
url: /zh/net/aspose.words.drawing.ole/forms2olecontrol/width/
---
## Forms2OleControl.Width property

获取或设置控件的宽度（以点为单位）。

```csharp
public double Width { get; set; }
```

## 例子

展示如何设置 ActiveX 控件的属性。

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;
oleControl.ForeColor = Color.FromArgb(0x17, 0xE1, 0x35);
oleControl.BackColor = Color.FromArgb(0x33, 0x97, 0xF4);
oleControl.Height = 100.54;
oleControl.Width = 201.06;
```

### 也可以看看

* class [Forms2OleControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
