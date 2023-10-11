---
title: Enum LayoutFlow
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.LayoutFlow uppräkning. Bestämmer flödet av textlayouten i en textruta.
type: docs
weight: 1100
url: /sv/net/aspose.words.drawing/layoutflow/
---
## LayoutFlow enumeration

Bestämmer flödet av textlayouten i en textruta.

```csharp
public enum LayoutFlow
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Horizontal | `0` | Text visas horisontellt. |
| TopToBottomIdeographic | `1` | Ideografisk text visas vertikalt. |
| BottomToTop | `2` | Text visas vertikalt. |
| TopToBottom | `3` | Text visas vertikalt. |
| HorizontalIdeographic | `4` | Ideografisk text visas horisontellt. |
| Vertical | `5` | Text visas vertikalt. |

### Exempel

Visar hur man lägger till text i en textruta och ändrar dess orientering

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

### Se även

* property [LayoutFlow](../textbox/layoutflow/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)


