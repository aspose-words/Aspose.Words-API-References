---
title: Forms2OleControl.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words for .NET
description: Forms2OleControl Width property. Gets or sets a width of the control in points in C#.
type: docs
weight: 100
url: /net/aspose.words.drawing.ole/forms2olecontrol/width/
---
## Forms2OleControl.Width property

Gets or sets a width of the control in points.

```csharp
public double Width { get; set; }
```

## Examples

Shows how to set properties for ActiveX control.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;
oleControl.ForeColor = Color.FromArgb(0x17, 0xE1, 0x35);
oleControl.BackColor = Color.FromArgb(0x33, 0x97, 0xF4);
oleControl.Height = 100.54;
oleControl.Width = 201.06;
```

### See Also

* class [Forms2OleControl](../)
* namespace [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../../)
