---
title: Forms2OleControl.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words for .NET
description: Adjust the Forms2OleControl's height property effortlessly in points for optimal display and functionality. Enhance your UI with precise control dimensions!
type: docs
weight: 70
url: /net/aspose.words.drawing.ole/forms2olecontrol/height/
---
## Forms2OleControl.Height property

Gets or sets a height of the control in points.

```csharp
public double Height { get; set; }
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
