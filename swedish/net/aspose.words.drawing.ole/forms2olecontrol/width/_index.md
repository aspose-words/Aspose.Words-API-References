---
title: Forms2OleControl.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words för .NET
description: Upptäck hur du enkelt justerar egenskapen Width i Forms2OleControl för exakt kontrollstorlek i punkter. Förbättra din UI-design utan ansträngning!
type: docs
weight: 100
url: /sv/net/aspose.words.drawing.ole/forms2olecontrol/width/
---
## Forms2OleControl.Width property

Hämtar eller ställer in en bredd på kontrollen i punkter.

```csharp
public double Width { get; set; }
```

## Exempel

Visar hur man anger egenskaper för ActiveX-kontroller.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;
oleControl.ForeColor = Color.FromArgb(0x17, 0xE1, 0x35);
oleControl.BackColor = Color.FromArgb(0x33, 0x97, 0xF4);
oleControl.Height = 100.54;
oleControl.Width = 201.06;
```

### Se även

* class [Forms2OleControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
