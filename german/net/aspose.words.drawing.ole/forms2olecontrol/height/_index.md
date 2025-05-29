---
title: Forms2OleControl.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words für .NET
description: Passen Sie die Höheneigenschaft des Forms2OleControls mühelos in Punkten an, um optimale Anzeige und Funktionalität zu gewährleisten. Verbessern Sie Ihre Benutzeroberfläche mit präzisen Steuerelementdimensionen!
type: docs
weight: 70
url: /de/net/aspose.words.drawing.ole/forms2olecontrol/height/
---
## Forms2OleControl.Height property

Ruft die Höhe des Steuerelements in Punkten ab oder legt sie fest.

```csharp
public double Height { get; set; }
```

## Beispiele

Zeigt, wie Eigenschaften für ActiveX-Steuerelemente festgelegt werden.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;
oleControl.ForeColor = Color.FromArgb(0x17, 0xE1, 0x35);
oleControl.BackColor = Color.FromArgb(0x33, 0x97, 0xF4);
oleControl.Height = 100.54;
oleControl.Width = 201.06;
```

### Siehe auch

* class [Forms2OleControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
