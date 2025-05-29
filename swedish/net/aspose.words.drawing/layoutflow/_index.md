---
title: LayoutFlow Enum
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.LayoutFlow-enum för att styra textlayout i textrutor, vilket enkelt förbättrar dokumentdesignen och läsbarheten.
type: docs
weight: 1430
url: /sv/net/aspose.words.drawing/layoutflow/
---
## LayoutFlow enumeration

Bestämmer flödet för textlayouten i en textruta.

```csharp
public enum LayoutFlow
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Horizontal | `0` | Texten visas horisontellt. |
| TopToBottomIdeographic | `1` | Ideografisk text visas vertikalt. |
| BottomToTop | `2` | Texten visas vertikalt. |
| TopToBottom | `3` | Texten visas vertikalt. |
| HorizontalIdeographic | `4` | Ideografisk text visas horisontellt. |
| Vertical | `5` | Texten visas vertikalt. |

## Exempel

Visar hur man lägger till text i en textruta och ändrar dess orientering

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

### Se även

* property [LayoutFlow](../textbox/layoutflow/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
