---
title: Forms2OleControl.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words för .NET
description: Justera Forms2OleControls höjdfunktion enkelt i punkter för optimal visning och funktionalitet. Förbättra ditt användargränssnitt med exakta kontrolldimensioner!
type: docs
weight: 70
url: /sv/net/aspose.words.drawing.ole/forms2olecontrol/height/
---
## Forms2OleControl.Height property

Hämtar eller ställer in en höjd på kontrollen i punkter.

```csharp
public double Height { get; set; }
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
