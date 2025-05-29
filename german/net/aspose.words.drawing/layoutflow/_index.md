---
title: LayoutFlow Enum
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.LayoutFlow, um das Textlayout in Textfeldern zu steuern und so mühelos das Design und die Lesbarkeit Ihres Dokuments zu verbessern.
type: docs
weight: 1430
url: /de/net/aspose.words.drawing/layoutflow/
---
## LayoutFlow enumeration

Bestimmt den Fluss des Textlayouts in einem Textfeld.

```csharp
public enum LayoutFlow
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Horizontal | `0` | Text wird horizontal angezeigt. |
| TopToBottomIdeographic | `1` | Ideografischer Text wird vertikal angezeigt. |
| BottomToTop | `2` | Text wird vertikal angezeigt. |
| TopToBottom | `3` | Text wird vertikal angezeigt. |
| HorizontalIdeographic | `4` | Ideografischer Text wird horizontal angezeigt. |
| Vertical | `5` | Text wird vertikal angezeigt. |

## Beispiele

Zeigt, wie man Text zu einem Textfeld hinzufügt und seine Ausrichtung ändert

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100,
    Height = 100
};
textbox.TextBox.LayoutFlow = LayoutFlow.BottomToTop;

textbox.AppendChild(new Paragraph(doc));
builder.InsertNode(textbox);

builder.MoveTo(textbox.FirstParagraph);
builder.Write("This text is flipped 90 degrees to the left.");

doc.Save(ArtifactsDir + "Drawing.TextBox.docx");
```

### Siehe auch

* property [LayoutFlow](../textbox/layoutflow/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
