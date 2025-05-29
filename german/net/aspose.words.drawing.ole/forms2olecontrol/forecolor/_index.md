---
title: Forms2OleControl.ForeColor
linktitle: ForeColor
articleTitle: ForeColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die ForeColor-Eigenschaft von Forms2OleControl, um die Vordergrundfarbe Ihres Steuerelements einfach anzupassen. Verbessern Sie Ihre Benutzeroberfläche noch heute mit maßgeschneiderten Farboptionen!
type: docs
weight: 50
url: /de/net/aspose.words.drawing.ole/forms2olecontrol/forecolor/
---
## Forms2OleControl.ForeColor property

Ruft eine Vordergrundfarbe des Steuerelements ab oder legt diese fest. Der Standardwert hängt vom Typ des Steuerelements ab.

```csharp
public Color ForeColor { get; set; }
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
