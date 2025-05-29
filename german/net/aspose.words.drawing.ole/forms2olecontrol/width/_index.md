---
title: Forms2OleControl.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die Width-Eigenschaft von Forms2OleControl einfach anpassen, um die Steuerelementgröße in Punkten präzise festzulegen. Verbessern Sie Ihr UI-Design mühelos!
type: docs
weight: 100
url: /de/net/aspose.words.drawing.ole/forms2olecontrol/width/
---
## Forms2OleControl.Width property

Ruft die Breite des Steuerelements in Punkten ab oder legt sie fest.

```csharp
public double Width { get; set; }
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
