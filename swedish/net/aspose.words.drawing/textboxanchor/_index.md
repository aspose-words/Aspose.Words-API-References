---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.TextBoxAnchor uppräkning. Anger värden som används för vertikal justering av formtext i C#.
type: docs
weight: 1330
url: /sv/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

Anger värden som används för vertikal justering av formtext.

```csharp
public enum TextBoxAnchor
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Top | `0` | Texten är anpassad till toppen av textrutan. |
| Middle | `1` | Texten är justerad mot mitten av textrutan. |
| Bottom | `2` | Texten är justerad längst ner i textrutan. |
| TopCentered | `3` | Text justeras till toppen centrerad i textrutan. |
| MiddleCentered | `4` | Text justeras till mitten av textrutan. |
| BottomCentered | `5` | Texten är justerad längst ned i mitten av textrutan. |
| TopBaseline | `6` | Text justeras till den övre baslinjen i textrutan. |
| BottomBaseline | `7` | Text är justerad till den nedre baslinjen i textrutan. |
| TopCenteredBaseline | `8` | Text justeras till den övre centrerade baslinjen i textrutan. |
| BottomCenteredBaseline | `9` | Text är justerad mot den nedre centrerade baslinjen i textrutan. |

## Exempel

Visar hur man vertikalt justerar textinnehållet i en textruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Top" till
// justera texten i denna textruta med formens övre sida.
// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Middle" till
// justera texten i denna textruta till mitten av formen.
// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Bottom" till
// justera texten i den här textrutan till botten av formen.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Den vertikala justeringen av text inuti textrutor är tillgänglig från Microsoft Word 2007 och framåt.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
