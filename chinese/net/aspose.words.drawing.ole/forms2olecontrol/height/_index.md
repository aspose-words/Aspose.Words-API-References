---
title: Forms2OleControl.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words for .NET
description: 轻松调整 Forms2OleControl 的高度属性（以点为单位），实现最佳显示效果和功能。使用精确的控件尺寸增强您的 UI！
type: docs
weight: 70
url: /zh/net/aspose.words.drawing.ole/forms2olecontrol/height/
---
## Forms2OleControl.Height property

获取或设置控件的高度（以点为单位）。

```csharp
public double Height { get; set; }
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
