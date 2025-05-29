---
title: Forms2OleControl.BackColor
linktitle: BackColor
articleTitle: BackColor
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Forms2OleControl BackColor för att anpassa din kontrolls bakgrundsfärg. Förbättra ditt användargränssnitt med flexibla färgalternativ idag!
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.ole/forms2olecontrol/backcolor/
---
## Forms2OleControl.BackColor property

Hämtar eller anger en bakgrundsfärg för kontrollen. Standardvärdet beror på kontrollens typ.

```csharp
public Color BackColor { get; set; }
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
