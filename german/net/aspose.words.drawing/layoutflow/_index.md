---
title: LayoutFlow Enum
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.LayoutFlow opsomming. Bestimmt den Fluss des Textlayouts in einem Textfeld in C#.
type: docs
weight: 1100
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

Zeigt, wie man einem Textfeld Text hinzufügt und seine Ausrichtung ändert

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100, 
    Height = 100,
    TextBox = { LayoutFlow = LayoutFlow.BottomToTop }
};

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
