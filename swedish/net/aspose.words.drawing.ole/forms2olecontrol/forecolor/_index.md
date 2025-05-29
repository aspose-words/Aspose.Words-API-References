---
title: Forms2OleControl.ForeColor
linktitle: ForeColor
articleTitle: ForeColor
second_title: Aspose.Words för .NET
description: Upptäck Forms2OleControl ForeColor-egenskapen för att enkelt anpassa din kontrolls förgrundsfärg. Förbättra ditt användargränssnitt med skräddarsydda färgalternativ idag!
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.ole/forms2olecontrol/forecolor/
---
## Forms2OleControl.ForeColor property

Hämtar eller ställer in en förgrundsfärg för kontrollen. Standardvärdet beror på kontrollens typ.

```csharp
public Color ForeColor { get; set; }
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
